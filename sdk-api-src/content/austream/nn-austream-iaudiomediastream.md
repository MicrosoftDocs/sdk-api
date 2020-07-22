---
UID: NN:austream.IAudioMediaStream
title: IAudioMediaStream (austream.h)
description: Note  This interface is deprecated.
helpviewer_keywords: ["IAudioMediaStream","IAudioMediaStream interface [DirectShow]","IAudioMediaStream interface [DirectShow]","described","IAudioMediaStreamInterface","austream/IAudioMediaStream","dshow.iaudiomediastream"]
old-location: dshow\iaudiomediastream.htm
tech.root: dshow
ms.assetid: b4098876-6c11-4cc6-8b6d-16edc02316f3
ms.date: 12/05/2018
ms.keywords: IAudioMediaStream, IAudioMediaStream interface [DirectShow], IAudioMediaStream interface [DirectShow],described, IAudioMediaStreamInterface, austream/IAudioMediaStream, dshow.iaudiomediastream
f1_keywords:
- austream/IAudioMediaStream
dev_langs:
- c++
req.header: austream.h
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
- austream.h
api_name:
- IAudioMediaStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioMediaStream interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IAudioMediaStream</code> interface controls audio media streams by providing methods that set and get the stream's format. This interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a> interface and is used to create one or more <a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiostreamsample">IAudioStreamSample</a> objects. You can also use it to set and retrieve the stream data's current format.

This interface is currently defined only for PCM format audio data.

For sample code that implements the audio streaming interfaces, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/multimedia-streaming-sample-code">Multimedia Streaming Sample Code</a>.

Like video, audio is contained in a self-describing container object. Implement this interface when an object needs to control streaming audio.

Use this interface when you want to generate audio in your application.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioMediaStream</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a>. <b>IAudioMediaStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioMediaStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/austream/nf-austream-iaudiomediastream-createsample">CreateSample</a>
</td>
<td align="left" width="63%">
Creates an audio stream sample for use with this stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/austream/nf-austream-iaudiomediastream-getformat">GetFormat</a>
</td>
<td align="left" width="63%">
Retrieves the stream data's current format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/austream/nf-austream-iaudiomediastream-setformat">SetFormat</a>
</td>
<td align="left" width="63%">
Sets the format for the stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nn-mmstream-imediastream">IMediaStream</a>
 

 

