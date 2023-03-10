---
UID: NF:mfobjects.IMFByteStream.Close
title: IMFByteStream::Close (mfobjects.h)
description: Closes the stream and releases any resources associated with the stream, such as sockets or file handles. This method also cancels any pending asynchronous I/O requests.
helpviewer_keywords: ["Close","Close method [Media Foundation]","Close method [Media Foundation]","IMFByteStream interface","IMFByteStream interface [Media Foundation]","Close method","IMFByteStream.Close","IMFByteStream::Close","d5f704ab-fa3f-4a53-9b97-eb48a75e481b","mf.imfbytestream_close","mfobjects/IMFByteStream::Close"]
old-location: mf\imfbytestream_close.htm
tech.root: mf
ms.assetid: d5f704ab-fa3f-4a53-9b97-eb48a75e481b
ms.date: 12/05/2018
ms.keywords: Close, Close method [Media Foundation], Close method [Media Foundation],IMFByteStream interface, IMFByteStream interface [Media Foundation],Close method, IMFByteStream.Close, IMFByteStream::Close, d5f704ab-fa3f-4a53-9b97-eb48a75e481b, mf.imfbytestream_close, mfobjects/IMFByteStream::Close
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFByteStream::Close
 - mfobjects/IMFByteStream::Close
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFByteStream.Close
---

# IMFByteStream::Close


## -description

Closes the stream and releases any resources associated with the stream, such as sockets or file handles. This method also cancels any pending asynchronous I/O requests.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>
