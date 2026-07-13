---
UID: NF:mfobjects.IMFByteStream.BeginRead
title: IMFByteStream::BeginRead (mfobjects.h)
description: Begins an asynchronous read operation from the stream.
helpviewer_keywords: ["BeginRead","BeginRead method [Media Foundation]","BeginRead method [Media Foundation]","IMFByteStream interface","IMFByteStream interface [Media Foundation]","BeginRead method","IMFByteStream.BeginRead","IMFByteStream::BeginRead","ed4aaf2a-270c-4518-b04d-cdac966bf9a5","mf.imfbytestream_beginread","mfobjects/IMFByteStream::BeginRead"]
old-location: mf\imfbytestream_beginread.htm
tech.root: mf
ms.assetid: ed4aaf2a-270c-4518-b04d-cdac966bf9a5
ms.date: 12/05/2018
ms.keywords: BeginRead, BeginRead method [Media Foundation], BeginRead method [Media Foundation],IMFByteStream interface, IMFByteStream interface [Media Foundation],BeginRead method, IMFByteStream.BeginRead, IMFByteStream::BeginRead, ed4aaf2a-270c-4518-b04d-cdac966bf9a5, mf.imfbytestream_beginread, mfobjects/IMFByteStream::BeginRead
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
 - IMFByteStream::BeginRead
 - mfobjects/IMFByteStream::BeginRead
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
 - IMFByteStream.BeginRead
---

# IMFByteStream::BeginRead


## -description

Begins an asynchronous read operation from the stream.

## -parameters

### -param pb [in]

Pointer to a buffer that receives the data. The caller must allocate the buffer.

### -param cb [in]

Size of the buffer in bytes.

### -param pCallback [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.

### -param punkState [in]

Pointer to the <b>IUnknown</b> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When all of the data has been read into the buffer, the callback object's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method is called. At that point, the application should call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread">IMFByteStream::EndRead</a> to complete the asynchronous request.
      

Do not read from, write to, free, or reallocate the buffer while an asynchronous read is pending.
      

<b> Implementation notes:</b>This method should update the current position in the stream by adding the number of bytes that will be read, which is specified by the value returned in the <i>pcbRead</i> parameter,  to the current position. Other methods that can update the current position are <b>BeginRead</b>, <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write">Write</a>, <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginwrite">BeginWrite</a>, <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-seek">Seek</a>, and <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-setcurrentposition">SetCurrentPosition</a>. 


This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>