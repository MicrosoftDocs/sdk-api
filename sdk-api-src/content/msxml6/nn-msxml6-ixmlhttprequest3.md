---
UID: NN:msxml6.IXMLHTTPRequest3
title: IXMLHTTPRequest3 (msxml6.h)
author: windows-sdk-content
description: Provides the methods and properties needed to configure and send HTTP requests and use callbacks to receive notifications during HTTP response processing.
old-location: ixhr2\ixmlhttprequest3.htm
tech.root: ixhr2
ms.assetid: 66af3f84-585c-441e-b9be-4ec188d72a19
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXMLHTTPRequest3, IXMLHTTPRequest3 interface [XMLHttpRequest2], IXMLHTTPRequest3 interface [XMLHttpRequest2],described, ixhr2.ixmlhttprequest3, msxml6/IXMLHTTPRequest3
ms.topic: interface
f1_keywords: 
 - "msxml6/IXMLHTTPRequest3"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXMLHTTPRequest3 interface


## -description


Provides the methods and properties needed to configure and send HTTP requests and use  callbacks  to receive notifications  during HTTP response processing. Derives from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a> interface. <div class="alert"><b>Note</b>  This interface is supported on Windows Phone 8.1. </div>
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ixhr2/ixmlhttprequest3-setclientcertificate">IXMLHTTPRequest3::SetClientCertificate</a>
</td>
<td align="left" width="63%">
Sets a client certificate to be used to authenticate against the URL specified in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-open">Open</a> method.

</td>
</tr>
</table> 


## -remarks



The <b>IXMLHTTPRequest3</b> interface configures and sends HTTP requests and uses  callbacks  to receive notifications  during HTTP response processing. The <b>IXMLHTTPRequest3</b> interface allows apps to run in a multi-threaded apartment (MTA), a requirement for running under the Windows Runtime (WinRT).

The <b>IXMLHTTPRequest3</b> interface extends the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a> interface.

The <b>IXMLHTTPRequest3</b> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3callback">IXMLHTTPRequest3Callback</a> interfaces extend the features provided by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2callback">IXMLHTTPRequest2Callback</a> interfaces with these additions:


<ul>
<li>Allows setting a client certificate to use for the HTTPS request with the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ixhr2/ixmlhttprequest3-setclientcertificate">SetClientCertificate</a>method on the <b>IXMLHTTPRequest3</b> interface.</li>
<li>Allows getting an issuer list to help filter down eligible client certificates to use for the next HTTP request with the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest3callback-onclientcertificaterequested">OnClientCertificateRequested</a>method on the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3callback">IXMLHTTPRequest3Callback</a> interface.</li>
<li>Allows ignoring certain certificate errors which would have otherwise aborted the HTTPS connection. </li>
<li>Allows getting certificate errors and the server certificate chain from the HTTPS response with the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest3callback-onservercertificatereceived">OnServerCertificateReceived</a>method on the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3callback">IXMLHTTPRequest3Callback</a> interface.</li>
</ul>


The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setproperty">SetProperty</a> method on the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a> interface is extended on the <b>IXMLHTTPRequest3</b> interface with new properties to support new scenarios:


<ul>
<li>XHR_PROP_NO_CACHE – Suppresses cache reads and writes for the HTTP request.</li>
<li>XHR_PROP_EXTENDED_ERROR – Causes the HTTP stack to provide HRESULTS with the underlying Win32 error code to the OnError method in case of failure.</li>
<li>XHR_PROP_QUERY_STRING_UTF8 – Causes the query string to be encoded in UTF-8 instead of ACP for HTTP request.</li>
<li>XHR_PROP_IGNORE_CERT_ERRORS – Suppresses certain server certificate errors.</li>
</ul>





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2callback">IXMLHTTPRequest2Callback</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3callback">IXMLHTTPRequest3Callback</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setproperty">SetProperty</a>
 

 

