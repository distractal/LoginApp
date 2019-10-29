Hello!

This application is mostly just for fun/portfolio, to show that I am capable of writing from FrontEnd to BackEnd a login application.

I wanted to gain some familiarity with the JAMstack (JavaScript / APIs / Markup) concept, as well as learn a bit of TypeScript.

I am planning on using Gridsome / VUE.js for the FrontEnd, and using that to make API calls to a simple BackEnd HTTP(S) API server written in Rust and serving PostgreSQL.

The framework I had planned to use to serve the API over Rust does not have built-in TLS, and to implement it programatically is kind of outside of the scope of the original project I was intending to make, so what I will likely do instead is set up a simple NGINX reverse proxy with SSL edge termination, and ferry traffic through Cloudflare.

Here's the plan:
- Determine the API layout / scheme
- Code the API / glue with placeholders for database calls
- Create an Azure VM running Ubuntu
- Set up the requisite virtual network and network security group in Azure
- Configure UFW to restrict inbound traffic to http/s access from anywhere, and ssh access ONLY from my IP address
- Configure NGINX / Cloudflare for SSL edge termination
- Configure NGINX to redirect http to https
- Configure Cloudflare DNS for distractal.com to point to Azure VM
- Compile my code on the Azure VM and confirm it works
- Redirect calls from https://loginapp.distractal.com to https://loginapp/distractal.com/API/whatever/blah/blah

....

TO BE CONTINUED :)