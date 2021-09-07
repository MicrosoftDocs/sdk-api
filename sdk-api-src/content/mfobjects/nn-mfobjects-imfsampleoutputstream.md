---
UID: NN:mfobjects.IMFSampleOutputStream
title: IMFSampleOutputStream (mfobjects.h)
description: Writes media samples to a byte stream.
helpviewer_keywords: ["IMFSampleOutputStream","IMFSampleOutputStream interface [Media Foundation]","IMFSampleOutputStream interface [Media Foundation]","described","mf.imfsampleoutputstream","mfobjects/IMFSampleOutputStream"]
old-location: mf\imfsampleoutputstream.htm
tech.root: mf
ms.assetid: BA293BB7-9191-4123-96DB-FF6386ABB3AE
ms.date: 12/05/2018
ms.keywords: IMFSampleOutputStream, IMFSampleOutputStream interface [Media Foundation], IMFSampleOutputStream interface [Media Foundation],described, mf.imfsampleoutputstream, mfobjects/IMFSampleOutputStream
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
 - IMFSampleOutputStream
 - mfobjects/IMFSampleOutputStream
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
 - IMFSampleOutputStream
---

# IMFSampleOutputStream interface


## -description

Writes media samples to a byte stream.

## -inheritance

The <b>IMFSampleOutputStream</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSampleOutputStream</b> also has these types of members:

## -remarks

A writable byte stream can optionally implement this interface. 

This interface enables the caller to send media samples to the byte stream for writing, instead of using the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginwrite">IMFByteStream::BeginWrite</a> method to write blobs of untyped data. The byte stream can use the information contained in the media sample to optimize how it writes the data. For example, a byte stream that sends media data over a network can optimize based on the time stamp.

To get a pointer to this interface, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the byte stream object.

Any implementation of <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> that exposes <b>IMFSampleOutputStream</b> as an interface needs to honor the following requirements:

<ul>
<li> All writes from either interface always go to the exact same byte stream object.
</li>
<li>The current position for both <b>IMFSampleOutputStream</b> and <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> shall always be the same. For example, writing to <b>IMFSampleOutputStream</b> will also update the current position of  <b>IMFByteStream</b>.
</li>
<li>Writing a sample using <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsampleoutputstream-beginwritesample">BeginWriteSample</a> and <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsampleoutputstream-endwritesample">EndWriteSample</a> shall serialize the sample by writing the data from all the buffers in the sample, in the order in which the buffers are stored in the sample.  (Use <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex">IMFSample::GetBufferByIndex</a> to get the individual buffers by index value.) The total bytes copied shall be the number of bytes written from all the buffers. </li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
