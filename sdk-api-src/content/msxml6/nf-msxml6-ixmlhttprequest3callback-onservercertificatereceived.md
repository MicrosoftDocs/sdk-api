---
UID: NF:msxml6.IXMLHTTPRequest3Callback.OnServerCertificateReceived
title: IXMLHTTPRequest3Callback::OnServerCertificateReceived
author: windows-sdk-content
description: Occurs when a client receives certificate errors or a server certificate chain during SSL negotiation with the server.
old-location: ixhr2\ixmlhttprequest3callback_onservercertificatereceived.htm
old-project: ixhr2
ms.assetid: 5b00ab76-880b-4450-a6b2-fda399cc9e8b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IXMLHTTPRequest3Callback interface [XMLHttpRequest2],OnServerCertificateReceived method, IXMLHTTPRequest3Callback.OnServerCertificateReceived, IXMLHTTPRequest3Callback::OnServerCertificateReceived, OnServerCertificateReceived, OnServerCertificateReceived method [XMLHttpRequest2], OnServerCertificateReceived method [XMLHttpRequest2],IXMLHTTPRequest3Callback interface, ixhr2.ixmlhttprequest3callback_onservercertificatereceived, msxml6/IXMLHTTPRequest3Callback::OnServerCertificateReceived
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msxml6.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msxml6.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XHR_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msxml6.h
api_name:
 - IXMLHTTPRequest3Callback.OnServerCertificateReceived
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IXMLHTTPRequest3Callback::OnServerCertificateReceived


## -description


Occurs when a client receives certificate errors or a server certificate chain during SSL negotiation with the server.


## -parameters




### -param pXHR [in]

The initial HTTP request.


### -param dwCertificateErrors [in]

The certificate errors encountered in the HTTPS connection (see XHR_CERT_ERROR_FLAG).


### -param cServerCertificateChain [in]

The number of elements in the <i>rgServerCertChain</i> parameter.


### -param rgServerCertificateChain [in]

An array of <a href="https://msdn.microsoft.com/0BBA4BDA-9A63-44A6-9B90-33B3EAE253C1">XHR_CERT</a> structures that represent the server certificate chain.


## -returns



Returns <b>S_OK</b> on success.




## -remarks



<div class="alert"><b>Note</b>  This callback method must not throw exceptions.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a>



<a href="https://msdn.microsoft.com/f745669a-a594-457d-ae6b-952a55576bae">IXMLHTTPRequest3Callback</a>



<a href="https://msdn.microsoft.com/4BBA4E21-29ED-413D-90D6-161D31CC13C9">SetProperty</a>



<a href="https://msdn.microsoft.com/0BBA4BDA-9A63-44A6-9B90-33B3EAE253C1">XHR_CERT</a>



<a href="https://msdn.microsoft.com/fb7ddd8a-aa00-4ca8-9516-f16e2b8df7b4">XHR_CERT_ERROR_FLAG</a>
 

 

