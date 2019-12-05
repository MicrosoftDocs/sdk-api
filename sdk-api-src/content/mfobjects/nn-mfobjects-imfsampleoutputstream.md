---
UID: NN:mfobjects.IMFSampleOutputStream
title: IMFSampleOutputStream (mfobjects.h)
description: Writes media samples to a byte stream.
old-location: mf\imfsampleoutputstream.htm
tech.root: medfound
ms.assetid: BA293BB7-9191-4123-96DB-FF6386ABB3AE
ms.date: 12/05/2018
ms.keywords: IMFSampleOutputStream, IMFSampleOutputStream interface [Media Foundation], IMFSampleOutputStream interface [Media Foundation],described, mf.imfsampleoutputstream, mfobjects/IMFSampleOutputStream
ms.topic: interface
f1_keywords:
- mfobjects/IMFSampleOutputStream
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfobjects.h
api_name:
- IMFSampleOutputStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSampleOutputStream interface


## -description


Writes media samples to a byte stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSampleOutputStream</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSampleOutputStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSampleOutputStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfsampleoutputstream-beginwritesample">BeginWriteSample</a>
</td>
<td align="left" width="63%">
Begins an asynchronous request to write a media sample to the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfsampleoutputstream-endwritesample">EndWriteSample</a>
</td>
<td align="left" width="63%">
Completes an asynchronous request to write a media sample to the stream.

</td>
</tr>
</table> 


## -remarks



A writeable byte stream can optionally implement this interface. 

This interface enables the caller to send media samples to the byte stream for writing, instead of using the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginwrite">IMFByteStream::BeginWrite</a> method to write blobs of untyped data. The byte stream can use the information contained in the media sample to optimize how it writes the data. For example, a byte stream that sends media data over a network can optimize based on the time stamp.

To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> on the byte stream object.

Any implementation of <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> that exposes <b>IMFSampleOutputStream</b> as an interface needs to honor the following requirements:

<ul>
<li> All writes from either interface always go to the exact same byte stream object.
</li>
<li>The current position for both <b>IMFSampleOutputStream</b> and <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a> shall always be the same. For example, writing to <b>IMFSampleOutputStream</b> will also update the current position of  <b>IMFByteStream</b>.
</li>
<li>Writing a sample using <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfsampleoutputstream-beginwritesample">BeginWriteSample</a> and <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfsampleoutputstream-endwritesample">EndWriteSample</a> shall serialize the sample by writing the data from all the buffers in the sample, in the order in which the buffers are stored in the sample.  (Use <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex">IMFSample::GetBufferByIndex</a> to get the individual buffers by index value.) The total bytes copied shall be the number of bytes written from all the buffers. </li>
</ul>







## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

