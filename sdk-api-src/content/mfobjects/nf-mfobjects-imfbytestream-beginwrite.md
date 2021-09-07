---
UID: NF:mfobjects.IMFByteStream.BeginWrite
title: IMFByteStream::BeginWrite (mfobjects.h)
description: Begins an asynchronous write operation to the stream.
helpviewer_keywords: ["078a8ffe-7b4f-487e-8655-fe5ea14ba306","BeginWrite","BeginWrite method [Media Foundation]","BeginWrite method [Media Foundation]","IMFByteStream interface","IMFByteStream interface [Media Foundation]","BeginWrite method","IMFByteStream.BeginWrite","IMFByteStream::BeginWrite","mf.imfbytestream_beginwrite","mfobjects/IMFByteStream::BeginWrite"]
old-location: mf\imfbytestream_beginwrite.htm
tech.root: mf
ms.assetid: 078a8ffe-7b4f-487e-8655-fe5ea14ba306
ms.date: 12/05/2018
ms.keywords: 078a8ffe-7b4f-487e-8655-fe5ea14ba306, BeginWrite, BeginWrite method [Media Foundation], BeginWrite method [Media Foundation],IMFByteStream interface, IMFByteStream interface [Media Foundation],BeginWrite method, IMFByteStream.BeginWrite, IMFByteStream::BeginWrite, mf.imfbytestream_beginwrite, mfobjects/IMFByteStream::BeginWrite
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
 - IMFByteStream::BeginWrite
 - mfobjects/IMFByteStream::BeginWrite
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
 - IMFByteStream.BeginWrite
---

# IMFByteStream::BeginWrite


## -description

Begins an asynchronous write operation to the stream.

## -parameters

### -param pb [in]

Pointer to a buffer containing the data to write.

### -param cb [in]

Size of the buffer in bytes.

### -param pCallback [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.

### -param punkState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When all of the data has been written to the stream, the callback object's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method is called. At that point, the application should call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endwrite">IMFByteStream::EndWrite</a> to complete the asynchronous request.
      

Do not reallocate, free, or write to the buffer while an asynchronous write is still pending.
      

<b>Implementation notes:</b>This method should update the current position in the stream by adding the number of bytes that will be written to the stream, which is specified by the value returned in the <i>pcbWritten</i>, to the current position. Other methods that can update the current position are <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read">Read</a>, <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread">BeginRead</a>, <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write">Write</a>, <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-seek">Seek</a>, and <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-setcurrentposition">SetCurrentPosition</a>.


This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>