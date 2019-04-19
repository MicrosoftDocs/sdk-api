---
UID: NF:wsdbase.IWSDSSLClientCertificate.GetClientCertificate
title: IWSDSSLClientCertificate::GetClientCertificate (wsdbase.h)
author: windows-sdk-content
description: Gets the client certificate.
old-location: ncd\iwsdsslclientcertificate_getclientcertificate.htm
tech.root: WsdApi
ms.assetid: 82f3f4ae-80fe-4382-9a22-00c70e99524f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetClientCertificate, GetClientCertificate method, GetClientCertificate method,IWSDSSLClientCertificate interface, IWSDSSLClientCertificate interface,GetClientCertificate method, IWSDSSLClientCertificate.GetClientCertificate, IWSDSSLClientCertificate::GetClientCertificate, ncd.iwsdsslclientcertificate_getclientcertificate, wsdbase/IWSDSSLClientCertificate::GetClientCertificate
ms.topic: method
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDSSLClientCertificate.GetClientCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDSSLClientCertificate::GetClientCertificate


## -description


Gets the client certificate.


## -parameters




### -param ppCertContext [in, out]

A pointer to a <a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure that contains the client SSL certificate.  Upon completion, the caller should free this memory by calling <a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>.


## -returns



Possible return values include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
A certificate is not available.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d1b5eb99-7bbb-4881-8251-4362368dff88">IWSDSSLClientCertificate</a>
 

 

