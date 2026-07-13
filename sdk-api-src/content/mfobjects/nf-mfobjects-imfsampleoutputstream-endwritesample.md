---
UID: NF:mfobjects.IMFSampleOutputStream.EndWriteSample
title: IMFSampleOutputStream::EndWriteSample (mfobjects.h)
description: Completes an asynchronous request to write a media sample to the stream.
helpviewer_keywords: ["EndWriteSample","EndWriteSample method [Media Foundation]","EndWriteSample method [Media Foundation]","IMFSampleOutputStream interface","IMFSampleOutputStream interface [Media Foundation]","EndWriteSample method","IMFSampleOutputStream.EndWriteSample","IMFSampleOutputStream::EndWriteSample","mf.imfsampleoutputstream_endwritesample","mfobjects/IMFSampleOutputStream::EndWriteSample"]
old-location: mf\imfsampleoutputstream_endwritesample.htm
tech.root: mf
ms.assetid: AE65CE63-B7FF-403B-ABB8-5E6C53CAD314
ms.date: 12/05/2018
ms.keywords: EndWriteSample, EndWriteSample method [Media Foundation], EndWriteSample method [Media Foundation],IMFSampleOutputStream interface, IMFSampleOutputStream interface [Media Foundation],EndWriteSample method, IMFSampleOutputStream.EndWriteSample, IMFSampleOutputStream::EndWriteSample, mf.imfsampleoutputstream_endwritesample, mfobjects/IMFSampleOutputStream::EndWriteSample
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
 - IMFSampleOutputStream::EndWriteSample
 - mfobjects/IMFSampleOutputStream::EndWriteSample
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
 - IMFSampleOutputStream.EndWriteSample
---

# IMFSampleOutputStream::EndWriteSample


## -description

Completes an asynchronous request to write a media sample to the stream.

## -parameters

### -param pResult [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. Pass in the same pointer that your callback object received in the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call this method when the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsampleoutputstream-beginwritesample">IMFSampleOutputStream::BeginWriteSample</a> method completes asynchronously.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsampleoutputstream">IMFSampleOutputStream</a>