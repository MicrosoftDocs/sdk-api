---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# VERIFYSERVERCERT callback function


## -description


<b>VERIFYSERVERCERT</b> is a callback function that allows a client to evaluate the certificate chain of the server to which it is connected.


## -parameters




### -param Connection

The session handle.


### -param *pServerCert








#### - ppServerCert

A pointer to a pointer to a session handle, represented by <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>.


## -returns



If the function succeeds (the client approves the server certificate), the return value is <b>TRUE</b>.

If the function fails; the return value is <b>FALSE</b> and the secure connection is torn down.




## -remarks



The <b>VERIFYSERVERCERT</b> callback function allows the client to verify the certificate of the server. The client registers a callback which is invoked after the secure connection is set up. The server certificate context is presented to the callback function, where it can be verified as acceptable or not. To register this callback, call 
<a href="https://msdn.microsoft.com/b6d6b285-7302-4812-bbcb-0aeb5b53cf23">ldap_set_option</a>where CertRoutine is the address of your callback function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>conn, LDAP_OPT_SERVER_CERTIFICATE, &amp;CertRoutine</pre>
</td>
</tr>
</table></span></div>
The server calls <b>VERIFYSERVERCERT</b> after the secure connection has been established. The server's certificate context is supplied for examination by the client.

An application should use the <i>ppServerCert</i> parameter as: <code>PCCERT_CONTEXT* ppServerCert = (PCCERT_CONTEXT*)pServerCert;</code>

Even though <b>VERIFYSERVERCERT</b> is declared as receiving a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">PCCERT_CONTEXT</a>, it in fact receives a <b>PCCERT_CONTEXT</b>*. The <i>ppServerCert</i> can be used to verify the certificate. <a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a> should be called before this function returns. The call to this function should be made as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CertFreeCertificateContext(*ppServerCert);</pre>
</td>
</tr>
</table></span></div>
Or, alternatively, as:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CertFreeCertificateContext(*((PCCERT_CONTEXT*)pServerCert));</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/b6d6b285-7302-4812-bbcb-0aeb5b53cf23">ldap_set_option</a>
 

 

