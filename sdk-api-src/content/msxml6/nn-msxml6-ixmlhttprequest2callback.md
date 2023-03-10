---
UID: NN:msxml6.IXMLHTTPRequest2Callback
title: IXMLHTTPRequest2Callback (msxml6.h)
description: Defines callbacks that notify an application with an outstanding IXMLHTTPRequest2 request of events that affect HTTP request and response processing. Note  This interface is supported on Windows Phone 8.1.  .
helpviewer_keywords: ["IXMLHTTPRequest2Callback","IXMLHTTPRequest2Callback interface [XMLHttpRequest2]","IXMLHTTPRequest2Callback interface [XMLHttpRequest2]","described","ixhr2.ixmlhttprequest2callback","msxml6/IXMLHTTPRequest2Callback"]
old-location: ixhr2\ixmlhttprequest2callback.htm
tech.root: ixhr2
ms.assetid: AA4B3F4C-6E28-458B-BE25-6CCE8865FC71
ms.date: 12/05/2018
ms.keywords: IXMLHTTPRequest2Callback, IXMLHTTPRequest2Callback interface [XMLHttpRequest2], IXMLHTTPRequest2Callback interface [XMLHttpRequest2],described, ixhr2.ixmlhttprequest2callback, msxml6/IXMLHTTPRequest2Callback
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
 - IXMLHTTPRequest2Callback
 - msxml6/IXMLHTTPRequest2Callback
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
 - IXMLHTTPRequest2Callback
---

# IXMLHTTPRequest2Callback interface


## -description

Defines callbacks that notify an application with an outstanding <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a>  request of events that affect HTTP request and response processing. <div class="alert"><b>Note</b>  This interface is supported on Windows Phone 8.1. </div>
<div> </div>

## -inheritance

The <b>IXMLHTTPRequest2Callback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IXMLHTTPRequest2Callback</b> also has these types of members:

## -remarks

Methods on the <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a> interface are asynchronous, so applications must pass an <b>IXMLHTTPRequest2Callback</b> object as a parameter in calls to <a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-open">Open</a> method on the <b>IXMLHTTPRequest2</b> interface to receive callback notifications. 

The <b>IXMLHTTPRequest2Callback</b> interface is extended by the <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3callback">IXMLHTTPRequest3Callback</a> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3">IXMLHTTPRequest3</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest3callback">IXMLHTTPRequest3Callback</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nf-msxml6-ixmlhttprequest2-open">Open</a>
