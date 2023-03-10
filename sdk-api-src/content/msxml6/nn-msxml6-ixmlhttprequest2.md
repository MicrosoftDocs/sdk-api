---
UID: NN:msxml6.IXMLHTTPRequest2
title: IXMLHTTPRequest2 (msxml6.h)
description: Provides the methods and properties needed to configure and send HTTP requests and use callbacks to receive notifications during HTTP response processing. Note  This interface is supported on Windows Phone 8.1.  .
helpviewer_keywords: ["IXMLHTTPRequest2","IXMLHTTPRequest2 interface [XMLHttpRequest2]","IXMLHTTPRequest2 interface [XMLHttpRequest2]","described","ixhr2.ixmlhttprequest2","msxml6/IXMLHTTPRequest2"]
old-location: ixhr2\ixmlhttprequest2.htm
tech.root: ixhr2
ms.assetid: BBC11C4A-AECF-4D6D-8275-3E852E309908
ms.date: 12/05/2018
ms.keywords: IXMLHTTPRequest2, IXMLHTTPRequest2 interface [XMLHttpRequest2], IXMLHTTPRequest2 interface [XMLHttpRequest2],described, ixhr2.ixmlhttprequest2, msxml6/IXMLHTTPRequest2
req.header: msxml6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps],MSXML 6.0 and later
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IXMLHTTPRequest2
 - msxml6/IXMLHTTPRequest2
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
 - IXMLHTTPRequest2
---

# IXMLHTTPRequest2 interface


## -description

Provides the methods and properties needed to configure and send HTTP requests and use  callbacks  to receive notifications  during HTTP response processing. <div class="alert"><b>Note</b>  This interface is supported on Windows Phone 8.1. </div>
<div> </div>

## -inheritance

The <b>IXMLHTTPRequest2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXMLHTTPRequest2</b> also has these types of members:

## -remarks

The <b>IXMLHTTPRequest2</b> interface is extended by the <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3">IXMLHTTPRequest3</a> interface. The <b>IXMLHTTPRequest3</b> inherits all the methods and properties of the <b>IXMLHTTPRequest2</b> interface.

The <b>IXMLHTTPRequest2</b> interface configures and sends HTTP request operations and uses  callbacks  to receive notifications  during response processing. The <b>IXMLHTTPRequest2</b> allows applications to run in a Multi Threaded Apartment (MTA), a requirement for running under the Windows Runtime (WinRT).

The <b>IXMLHTTPRequest2</b> interface supports the following features:


<ul>
<li>Set properties on outgoing HTTP requests.</li>
<li>Set cookies in the HTTP cookie jar for use in outgoing HTTP requests.</li>
<li>Get cookies from the HTTP cookie jar.</li>
<li>Process incoming HTTP response data before the HTTP response has finished downloading.</li>
<li>Create custom streams to receive HTTP responses.</li>
</ul>


<b>IXMLHTTPRequest2</b> implements a callback model for event handling. Because <b>IXMLHTTPRequest2</b> methods allow only asynchronous method calls, to receive completion callbacks an application must pass a pointer to an <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2callback">IXMLHTTPRequest2Callback</a> object when it calls the <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-open">IXMLHTTPRequest2::Open</a> method to create an HTTP request.

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2callback">IXMLHTTPRequest2Callback</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3">IXMLHTTPRequest3</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3callback">IXMLHTTPRequest3Callback</a>



<a href="/previous-versions/windows/apps/hh770550(v=win.10)">Quickstart: Connecting using XML HTTP Request (IXHR2)</a>



<a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/XmlHttpRequest2GetRequest">XML HTTP Request 2 GET sample</a>


<a href="https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/XmlHttpRequest2PostRequest">XML HTTP Request 2 POST sample</a>
