---
UID: NF:mfobjects.IMFSampleOutputStream.BeginWriteSample
title: IMFSampleOutputStream::BeginWriteSample (mfobjects.h)
description: Begins an asynchronous request to write a media sample to the stream.
helpviewer_keywords: ["BeginWriteSample","BeginWriteSample method [Media Foundation]","BeginWriteSample method [Media Foundation]","IMFSampleOutputStream interface","IMFSampleOutputStream interface [Media Foundation]","BeginWriteSample method","IMFSampleOutputStream.BeginWriteSample","IMFSampleOutputStream::BeginWriteSample","mf.imfsampleoutputstream_beginwritesample","mfobjects/IMFSampleOutputStream::BeginWriteSample"]
old-location: mf\imfsampleoutputstream_beginwritesample.htm
tech.root: mf
ms.assetid: 41056795-3E12-448E-9341-FB4DD4E7D079
ms.date: 12/05/2018
ms.keywords: BeginWriteSample, BeginWriteSample method [Media Foundation], BeginWriteSample method [Media Foundation],IMFSampleOutputStream interface, IMFSampleOutputStream interface [Media Foundation],BeginWriteSample method, IMFSampleOutputStream.BeginWriteSample, IMFSampleOutputStream::BeginWriteSample, mf.imfsampleoutputstream_beginwritesample, mfobjects/IMFSampleOutputStream::BeginWriteSample
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMFSampleOutputStream::BeginWriteSample
 - mfobjects/IMFSampleOutputStream::BeginWriteSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.h
api_name:
 - IMFSampleOutputStream.BeginWriteSample
---

# IMFSampleOutputStream::BeginWriteSample


## -description

Begins an asynchronous request to write a media sample to the stream.

## -parameters

### -param pSample [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface of the sample.

### -param pCallback [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. The caller must implement this interface.

### -param punkState [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of a state object, defined by the caller. This parameter can be <b>NULL</b>. You can use this object to hold state information. The object is returned to the caller when the callback is invoked.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When the sample has been written to the stream, the callback object's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method is called. At that point, the caller should call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsampleoutputstream-endwritesample">IMFSampleOutputStream::EndWriteSample</a> to complete the asynchronous request.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsampleoutputstream">IMFSampleOutputStream</a>