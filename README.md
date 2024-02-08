# Calling a SOAP Service with REST

## Description
You can call A SOAP service with REST. SOAP, as a technology, is simply a Web (or HTTP) POST call with a specifically formatted XML payload, which the SOAP server is expecting and understands. It then returns a specifically formatted XML response that the client can parse and use.
Instead of an API reference, which gives you the Request and Response formats and requirements, SOAP publishes a WSDL. So if you’ve got one of these SOAP Services that breaks standards, if you can get the text of a successful request, you can use REST to make the call with that request body. I will use a free SOAP web service that works with countries to show you how this works.

Linx uses .NET services to call SOAP services, following the .Net defined standards. This means that there would be SOAP services that would not work with Linx directly, as they would break the .NET standards for SOAP.

A very important note to consider when it comes to working with XML / SOAP documents are the Namespaces. Namespaces are referenced in different places in an XML document and will cause you much trouble with Linx. When working with XML responses from a call, remove all Namespace references (including the object prefixes like m: or s: or h:) before trying to generate your new Scheme using the response data. Also, when reading the XML using XMLReader with the new “local” schema, remember to remove the Namespace prefixes.

## Installation
You will need the Linx 6 Designer; get it [here](https://linx.software/linx-download/)

## Usage
Download the project and open it in Linx. You can run it via debug mode. Add breakpoints to see exactly what the data looks like. 

## Contributing

For questions please ask the [Linx community](https://linx/software/community). 

## License

[MIT](https://github.com/linx-software/template-repo/blob/main/LICENSE.txt)
