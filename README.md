Tplmap
======

Tplmap (short for _Template Mapper_) is a tool that automate the process of detecting and exploiting Server-Side Template Injection vulnerabilities (SSTI). 

This can be used by developers, penetration testers, and security researchers to detect and exploit vulnerabilities related to the template injection attacks.

The technique can be used to compromise web servers' internals and often obtain Remote Code Execution (RCE), turning every vulnerable application into a potential pivot point.

The modular approach allows any contributor to extend the support to other templating engines or introduce new exploitation techniques. The majority of the techniques currently implemented came from the amazing research done by [James Kett, PortSwigger][1].

> The application is currently under heavy development and misses some functionalities.

Supported template engines
--------------------------

| Template engine    | Detection | command execution | Code evaluation | File read | File write |
|--------------------|-----------|-------------------|-----------------|-----------|------------|
| Mako               |  yes      | yes               | python          | yes       | yes        |
| Jinja2             |  yes      | yes               | python          | yes       | yes        |
| Jade               |  yes      | yes               | javascript      | yes       | yes        |
| Smarty (unsecured) |  yes      | yes               | PHP             | yes       | yes        |
| Freemarker         |  yes      | yes               | no              | yes       | yes        |
| Velocity           |  yes      | no                | no              | no        | no         |
| Twig               |  yes      | no                | no              | no        | no         |
| Smarty (secured)   |  yes      | no                | no              | no        | no         |


[1]: http://blog.portswigger.net/2015/08/server-side-template-injection.html
