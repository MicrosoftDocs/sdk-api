---
UID: NF:msxml6.IXMLHTTPRequest2.SetCustomResponseStream
title: IXMLHTTPRequest2::SetCustomResponseStream (msxml6.h)
description: Provides a custom stream to replace the standard stream for receiving an HTTP response.
helpviewer_keywords: ["IXMLHTTPRequest2 interface [XMLHttpRequest2]","SetCustomResponseStream method","IXMLHTTPRequest2.SetCustomResponseStream","IXMLHTTPRequest2::SetCustomResponseStream","SetCustomResponseStream","SetCustomResponseStream method [XMLHttpRequest2]","SetCustomResponseStream method [XMLHttpRequest2]","IXMLHTTPRequest2 interface","ixhr2.ixmlhttprequest2_setcustomresponsestream","msxml6/IXMLHTTPRequest2::SetCustomResponseStream"]
old-location: ixhr2\ixmlhttprequest2_setcustomresponsestream.htm
tech.root: ixhr2
ms.assetid: 64341C82-85EC-402F-A875-85706DFD7B25
ms.date: 12/05/2018
ms.keywords: IXMLHTTPRequest2 interface [XMLHttpRequest2],SetCustomResponseStream method, IXMLHTTPRequest2.SetCustomResponseStream, IXMLHTTPRequest2::SetCustomResponseStream, SetCustomResponseStream, SetCustomResponseStream method [XMLHttpRequest2], SetCustomResponseStream method [XMLHttpRequest2],IXMLHTTPRequest2 interface, ixhr2.ixmlhttprequest2_setcustomresponsestream, msxml6/IXMLHTTPRequest2::SetCustomResponseStream
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
 - IXMLHTTPRequest2::SetCustomResponseStream
 - msxml6/IXMLHTTPRequest2::SetCustomResponseStream
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
 - IXMLHTTPRequest2.SetCustomResponseStream
---

# IXMLHTTPRequest2::SetCustomResponseStream


## -description

Provides a custom stream to replace the standard stream for receiving an HTTP response.

## -parameters

### -param pSequentialStream

Custom stream that will receive the HTTP response. <a href="/windows/desktop/api/objidl/nn-objidl-isequentialstream">ISequentialStream</a>

## -returns

Returns <b>S_OK</b> on success.

## -remarks

After this method is called, <a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a> will call the <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-write">ISequentialStream::Write</a> method when it receives response data from the server. You can begin processing the data at that time, but avoid heavy processing because the call is made inline to receiving further data from the server. Because this <b>IXMLHTTPRequest2</b> never calls <a href="/windows/desktop/api/objidl/nf-objidl-isequentialstream-read">ISequentialStream::Read</a> on the custom stream, it is safe to return <b>E_NOTIMPL</b> if the application does not need to use <b>ISequentialStream::Read</b>.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-isequentialstream">ISequentialStream Interface</a>



<a href="/previous-versions/windows/desktop/api/msxml6/nn-msxml6-ixmlhttprequest2">IXMLHTTPRequest2</a>