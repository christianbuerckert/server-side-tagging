# Google's server-side tagging

Read: https://developers.google.com/tag-platform/tag-manager/server-side

This project helps to setup server-side tagging for google-analytics. Therefore a simple compose file will startup a single-node cluster for small setups which cannot afford a full cluster in a k8s environment.

Steps:
1. Create a server-side container in https://tagmanager.google.com/
2. Copy the configuration string
3. Create a virtual maschine and install docker & docker-compose
4. Add two subdomains to the VM
5. Copy the compose file 
6. Paste config string into the compose
7. Adapt subdomains
8. Fill in an e-mail address for acme
9. Start the compose
10. Configure your tags inside the tagmanager oon https://tagmanager.google.com/
11. Add the analytics scripts (and other tracking codes) to your homepage:

```
<script async="" src="https://gtm.example.com/analytics.js">
<script async src="https://gtm.example.com//gtag/js?id=UA-.......-.">
</script>
```

This is a very basic setup using a 5 € docker-vm to serve google analytics. However for big systems you should consider doing a k8s setup as described by google.
