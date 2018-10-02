---
UID: NN:msxml6.IXMLHTTPRequest3
title: IXMLHTTPRequest3
author: windows-sdk-content
description: Provides the methods and properties needed to configure and send HTTP requests and use callbacks to receive notifications during HTTP response processing.
old-location: ixhr2\ixmlhttprequest3.htm
tech.root: ixhr2
ms.assetid: 66af3f84-585c-441e-b9be-4ec188d72a19
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IXMLHTTPRequest3, IXMLHTTPRequest3 interface [XMLHttpRequest2], IXMLHTTPRequest3 interface [XMLHttpRequest2],described, ixhr2.ixmlhttprequest3, msxml6/IXMLHTTPRequest3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msxml6.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msxml6.h
api_name:
 - IXMLHTTPRequest3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXMLHTTPRequest3 interface


## -description


Provides the methods and properties needed to configure and send HTTP requests and use  callbacks  to receive notifications  during HTTP response processing. Derives from the <a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a> interface. <div class="alert"><b>Note</b>  This interface is supported on Windows Phone 8.1. </div>
<div> </div>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXMLHTTPRequest3</b> interface inherits from <b>IXMLHTTPRequest2</b>. <b>IXMLHTTPRequest3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXMLHTTPRequest3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc3e2645-666c-42af-babd-1f476b6356b8">IXMLHTTPRequest3::SetClientCertificate</a>
</td>
<td align="left" width="63%">
Sets a client certificate to be used to authenticate against the URL specified in the <a href="https://msdn.microsoft.com/8723F24B-0739-44D6-8443-1A378B585F42">Open</a> method.

</td>
</tr>
</table> 


## -remarks



The <b>IXMLHTTPRequest3</b> interface configures and sends HTTP requests and uses  callbacks  to receive notifications  during HTTP response processing. The <b>IXMLHTTPRequest3</b> interface allows apps to run in a multi-threaded apartment (MTA), a requirement for running under the Windows Runtime (WinRT).

The <b>IXMLHTTPRequest3</b> interface extends the <a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a> interface.

The <b>IXMLHTTPRequest3</b> and <a href="https://msdn.microsoft.com/f745669a-a594-457d-ae6b-952a55576bae">IXMLHTTPRequest3Callback</a> interfaces extend the features provided by the <a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a> and <a href="https://msdn.microsoft.com/AA4B3F4C-6E28-458B-BE25-6CCE8865FC71">IXMLHTTPRequest2Callback</a> interfaces with these additions:


<ul>
<li>Allows setting a client certificate to use for the HTTPS request with the <a href="https://msdn.microsoft.com/fc3e2645-666c-42af-babd-1f476b6356b8">SetClientCertificate</a>method on the <b>IXMLHTTPRequest3</b> interface.</li>
<li>Allows getting an issuer list to help filter down eligible client certificates to use for the next HTTP request with the <a href="https://msdn.microsoft.com/9c64fbb5-b755-4f1b-90f3-3cc414b3f5a4">OnClientCertificateRequested</a>method on the <a href="https://msdn.microsoft.com/f745669a-a594-457d-ae6b-952a55576bae">IXMLHTTPRequest3Callback</a> interface.</li>
<li>Allows ignoring certain certificate errors which would have otherwise aborted the HTTPS connection. </li>
<li>Allows getting certificate errors and the server certificate chain from the HTTPS response with the <a href="https://msdn.microsoft.com/5b00ab76-880b-4450-a6b2-fda399cc9e8b">OnServerCertificateReceived</a>method on the <a href="https://msdn.microsoft.com/f745669a-a594-457d-ae6b-952a55576bae">IXMLHTTPRequest3Callback</a> interface.</li>
</ul>


The <a href="https://msdn.microsoft.com/4BBA4E21-29ED-413D-90D6-161D31CC13C9">SetProperty</a> method on the <a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a> interface is extended on the <b>IXMLHTTPRequest3</b> interface with new properties to support new scenarios:


<ul>
<li>XHR_PROP_NO_CACHE – Suppresses cache reads and writes for the HTTP request.</li>
<li>XHR_PROP_EXTENDED_ERROR – Causes the HTTP stack to provide HRESULTS with the underlying Win32 error code to the OnError method in case of failure.</li>
<li>XHR_PROP_QUERY_STRING_UTF8 – Causes the query string to be encoded in UTF-8 instead of ACP for HTTP request.</li>
<li>XHR_PROP_IGNORE_CERT_ERRORS – Suppresses certain server certificate errors.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/BBC11C4A-AECF-4D6D-8275-3E852E309908">IXMLHTTPRequest2</a>



<a href="https://msdn.microsoft.com/AA4B3F4C-6E28-458B-BE25-6CCE8865FC71">IXMLHTTPRequest2Callback</a>



<a href="https://msdn.microsoft.com/f745669a-a594-457d-ae6b-952a55576bae">IXMLHTTPRequest3Callback</a>



<a href="https://msdn.microsoft.com/4BBA4E21-29ED-413D-90D6-161D31CC13C9">SetProperty</a>
 

 

