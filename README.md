# pluck CMS 4.7.18 Reflected XSS

## Author: (Sergio)

**Description:** Multiple Cross-Site Scripting (XSS) vulnerabilities in installation of PluckCMS v.4.7.18 allows a local attacker to execute arbitrary code via a crafted payload injected into the cont1 and cont2 parameters in the installation process- Website Name.

**Attack Vectors:** AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:L/A:L

---

### POC:


During the installation process we enter the XSS payload in any of the 2 parameters and when we click on next, we will obtain the XSS pop-up

### XSS Payload:

```js
<img src=x:alert(alt) onerror=eval(src) alt='XSS Page'>
```


In the following image you can see the embedded code that executes the payload in the instalaltion process.
![XSS Installation](https://github.com/sromanhu/-Pluck-CMS-Reflected-XSS---Installation/assets/87250597/a8176ca3-79f0-49b5-8068-396f085d1818)


And below is evidence of the execution of the payload when accessing the main website:
![XSS Resultado](https://github.com/sromanhu/-Pluck-CMS-Reflected-XSS---Installation/assets/87250597/efd33235-5dc4-4ab3-bfd5-f45202980b3d)




</br>

### Additional Information:

https://github.com/pluck-cms

https://owasp.org/Top10/es/A03_2021-Injection/

