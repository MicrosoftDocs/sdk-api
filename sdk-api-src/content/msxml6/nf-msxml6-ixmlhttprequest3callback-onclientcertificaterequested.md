---
UID: NF:msxml6.IXMLHTTPRequest3Callback.OnClientCertificateRequested
title: IXMLHTTPRequest3Callback::OnClientCertificateRequested
author: windows-sdk-content
description: Occurs when a client receives a request for a client certificate during SSL negotiation with the server.
old-location: ixhr2\ixmlhttprequest3callback_onclientcertificaterequested.htm
old-project: ixhr2
ms.assetid: 9c64fbb5-b755-4f1b-90f3-3cc414b3f5a4
ms.author: windowssdkdev
ms.date: 04/02/2018
ms.keywords: IXMLHTTPRequest3Callback interface [XMLHttpRequest2],OnClientCertificateRequested method, IXMLHTTPRequest3Callback.OnClientCertificateRequested, IXMLHTTPRequest3Callback::OnClientCertificateRequested, OnClientCertificateRequested, OnClientCertificateRequested method [XMLHttpRequest2], OnClientCertificateRequested method [XMLHttpRequest2],IXMLHTTPRequest3Callback interface, ixhr2.ixmlhttprequest3callback_onclientcertificaterequested, msxml6/IXMLHTTPRequest3Callback::OnClientCertificateRequested
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
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
 - IXMLHTTPRequest3Callback.OnClientCertificateRequested
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IXMLHTTPRequest3Callback::OnClientCertificateRequested


## -description


Occurs when a client receives a request for a client certificate during SSL negotiation with the server.


## -parameters




### -param pXHR [in]

The initial HTTP request.


### -param cIssuerList [in]

The number of strings in the <i>rgpwszIssuerList</i> parameter.


### -param rgpwszIssuerList [in]

An array of strings that represent the issuer list.


## -returns



Returns <b>S_OK</b> on success.




## -remarks



<div class="alert"><b>Note</b>  This callback method must not throw exceptions.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a>



<a href="https://msdn.microsoft.com/f745669a-a594-457d-ae6b-952a55576bae">IXMLHTTPRequest3Callback</a>



<a href="https://msdn.microsoft.com/4BBA4E21-29ED-413D-90D6-161D31CC13C9">SetProperty</a>
 

 

