---
UID: NN:msxml6.IXMLHTTPRequest3Callback
title: IXMLHTTPRequest3Callback (msxml6.h)
description: Defines callbacks that notify an application with an outstanding IXMLHTTPRequest3 request of events that affect HTTP request and response processing.
helpviewer_keywords: ["IXMLHTTPRequest3Callback","IXMLHTTPRequest3Callback interface [XMLHttpRequest2]","IXMLHTTPRequest3Callback interface [XMLHttpRequest2]","described","ixhr2.ixmlhttprequest3callback","msxml6/IXMLHTTPRequest3Callback"]
old-location: ixhr2\ixmlhttprequest3callback.htm
tech.root: ixhr2
ms.assetid: f745669a-a594-457d-ae6b-952a55576bae
ms.date: 12/05/2018
ms.keywords: IXMLHTTPRequest3Callback, IXMLHTTPRequest3Callback interface [XMLHttpRequest2], IXMLHTTPRequest3Callback interface [XMLHttpRequest2],described, ixhr2.ixmlhttprequest3callback, msxml6/IXMLHTTPRequest3Callback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXMLHTTPRequest3Callback
 - msxml6/IXMLHTTPRequest3Callback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msxml6.h
api_name:
 - IXMLHTTPRequest3Callback
---

# IXMLHTTPRequest3Callback interface


## -description

Defines callbacks that notify an application with an outstanding <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3">IXMLHTTPRequest3</a>  request of events that affect HTTP request and response processing. Derives from the <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2callback">IXMLHTTPRequest2Callback</a> interface. <div class="alert"><b>Note</b>  This interface is supported on Windows Phone 8.1. </div>
<div> </div>

## -inheritance

The <b>IXMLHTTPRequest3Callback</b> interface inherits from <b>IXMLHTTPRequest2Callback</b>. <b>IXMLHTTPRequest3Callback</b> also has these types of members:

## -remarks

The <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3">IXMLHTTPRequest3</a> and <b>IXMLHTTPRequest3Callback</b> interfaces extend the features provided by the <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a> and <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2callback">IXMLHTTPRequest2Callback</a> interfaces with these additions:


<ul>
<li>Allows setting a client certificate to use for the HTTPS request with the <a href="/previous-versions/windows/desktop/ixhr2/ixmlhttprequest3-setclientcertificate">SetClientCertificate</a> method on the <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3">IXMLHTTPRequest3</a> interface.</li>
<li>Allows getting an issuer list to help filter down eligible client certificates to use for the next HTTP request with the <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest3callback-onclientcertificaterequested">OnClientCertificateRequested</a> method on the <b>IXMLHTTPRequest3Callback</b> interface.</li>
<li>Allows ignoring certain certificate errors which would have otherwise aborted the HTTPS connection. </li>
<li>Allows getting certificate errors and the server certificate chain from the HTTPS response with the <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest3callback-onservercertificatereceived">OnServerCertificateReceived</a> method on the <b>IXMLHTTPRequest3Callback</b> interface.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2callback">IXMLHTTPRequest2Callback</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3">IXMLHTTPRequest3</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-setproperty">SetProperty</a>
