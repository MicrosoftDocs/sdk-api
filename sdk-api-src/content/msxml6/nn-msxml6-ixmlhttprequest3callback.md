---
UID: NN:msxml6.IXMLHTTPRequest3Callback
title: IXMLHTTPRequest3Callback
author: windows-driver-content
description: Defines callbacks that notify an application with an outstanding IXMLHTTPRequest3 request of events that affect HTTP request and response processing.
old-location: ixhr2\ixmlhttprequest3callback.htm
old-project: ixhr2
ms.assetid: f745669a-a594-457d-ae6b-952a55576bae
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IXMLHTTPRequest3Callback, IXMLHTTPRequest3Callback interface [XMLHttpRequest2], IXMLHTTPRequest3Callback interface [XMLHttpRequest2],described, ixhr2.ixmlhttprequest3callback, msxml6/IXMLHTTPRequest3Callback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: XHR_PROPERTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msxml6.h
api_name:
-	IXMLHTTPRequest3Callback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IXMLHTTPRequest3Callback interface


## -description


Defines callbacks that notify an application with an outstanding <a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a>  request of events that affect HTTP request and response processing. Derives from the <a href="https://msdn.microsoft.com/AA4B3F4C-6E28-458B-BE25-6CCE8865FC71">IXMLHTTPRequest2Callback</a> interface. <div class="alert"><b>Note</b>  This interface is supported on Windows Phone 8.1. </div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXMLHTTPRequest3Callback</b> interface inherits from <b>IXMLHTTPRequest2Callback</b>. <b>IXMLHTTPRequest3Callback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXMLHTTPRequest3Callback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c64fbb5-b755-4f1b-90f3-3cc414b3f5a4">IXMLHTTPRequest3Callback::OnClientCertificateRequested</a>
</td>
<td align="left" width="63%">
Occurs when a client receives a request for a client certificate during SSL negotiation with the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b00ab76-880b-4450-a6b2-fda399cc9e8b">IXMLHTTPRequest3Callback::OnServerCertificateReceived</a>
</td>
<td align="left" width="63%">
Occurs when a client receives certificate errors or a server certificate chain during SSL negotiation with the server.

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a> and <b>IXMLHTTPRequest3Callback</b> interfaces extend the features provided by the <a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a> and <a href="https://msdn.microsoft.com/AA4B3F4C-6E28-458B-BE25-6CCE8865FC71">IXMLHTTPRequest2Callback</a> interfaces with these additions:


<ul>
<li>Allows setting a client certificate to use for the HTTPS request with the <a href="https://msdn.microsoft.com/fc3e2645-666c-42af-babd-1f476b6356b8">SetClientCertificate</a>
method on the <a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a> interface.</li>
<li>Allows getting an issuer list to help filter down eligible client certificates to use for the next HTTP request with the <a href="https://msdn.microsoft.com/9c64fbb5-b755-4f1b-90f3-3cc414b3f5a4">OnClientCertificateRequested</a>
method on the <b>IXMLHTTPRequest3Callback</b> interface.</li>
<li>Allows ignoring certain certificate errors which would have otherwise aborted the HTTPS connection. </li>
<li>Allows getting certificate errors and the server certificate chain from the HTTPS response with the <a href="https://msdn.microsoft.com/5b00ab76-880b-4450-a6b2-fda399cc9e8b">OnServerCertificateReceived</a>
method on the <b>IXMLHTTPRequest3Callback</b> interface.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a>



<a href="https://msdn.microsoft.com/AA4B3F4C-6E28-458B-BE25-6CCE8865FC71">IXMLHTTPRequest2Callback</a>



<a href="https://msdn.microsoft.com/66af3f84-585c-441e-b9be-4ec188d72a19">IXMLHTTPRequest3</a>



<a href="https://msdn.microsoft.com/4BBA4E21-29ED-413D-90D6-161D31CC13C9">SetProperty</a>
 

 

