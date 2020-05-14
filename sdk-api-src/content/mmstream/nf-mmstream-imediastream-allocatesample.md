---
UID: NF:mmstream.IMediaStream.AllocateSample
title: IMediaStream::AllocateSample (mmstream.h)
description: Note  This interface is deprecated. New applications should not use it. Allocates a new stream sample object for the current media stream.helpviewer_keywords: ["AllocateSample","AllocateSample method [DirectShow]","AllocateSample method [DirectShow]","IMediaStream interface","IMediaStream interface [DirectShow]","AllocateSample method","IMediaStream.AllocateSample","IMediaStream::AllocateSample","IMediaStreamAllocateSample","dshow.imediastream_allocatesample","mmstream/IMediaStream::AllocateSample"]
old-location: dshow\imediastream_allocatesample.htm
tech.root: DirectShow
ms.assetid: a035797d-ebf2-40c2-b1a3-b903a691b7d2
ms.date: 12/05/2018
ms.keywords: AllocateSample, AllocateSample method [DirectShow], AllocateSample method [DirectShow],IMediaStream interface, IMediaStream interface [DirectShow],AllocateSample method, IMediaStream.AllocateSample, IMediaStream::AllocateSample, IMediaStreamAllocateSample, dshow.imediastream_allocatesample, mmstream/IMediaStream::AllocateSample
f1_keywords:
- mmstream/IMediaStream.AllocateSample
dev_langs:
- c++
req.header: mmstream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
- mmstream.h
api_name:
- IMediaStream.AllocateSample
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaStream::AllocateSample


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Allocates a new stream sample object for the current media stream.




## -parameters




### -param dwFlags [in]

Flags. Must be zero.


### -param ppSample [out]

Address of a pointer to the newly created stream sample's <a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample</a> interface.


## -returns



Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There isn't enough memory available to create a stream sample.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



This method allocates the sample and its associated backing object or buffer. The backing object is either the DirectDraw surface for video or the <a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiodata">IAudioData</a> object for audio.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream Interface</a>
 

 

