---
UID: NN:austream.IAudioStreamSample
title: IAudioStreamSample (austream.h)
author: windows-sdk-content
description: Note  This interface is deprecated.
old-location: dshow\iaudiostreamsample.htm
tech.root: DirectShow
ms.assetid: 53deec43-30ca-472e-9a82-750049686d2a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAudioStreamSample, IAudioStreamSample interface [DirectShow], IAudioStreamSample interface [DirectShow],described, IAudioStreamSampleInterface, austream/IAudioStreamSample, dshow.iaudiostreamsample
ms.topic: interface
f1_keywords: 
 - "austream/IAudioStreamSample"
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
 - IAudioStreamSample
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioStreamSample interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IAudioStreamSample</code> interface retrieves information from the underlying <a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiodata">IAudioData</a> data objects.

For sample code that implements the audio streaming interfaces, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/multimedia-streaming-sample-code">Multimedia Streaming Sample Code</a>.

Implement this interface on audio stream sample objects when they need access to an <a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiodata">IAudioData</a> object's data.

Use this interface when your application needs to access an <a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiodata">IAudioData</a> object's data for its audio stream.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioStreamSample</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample</a>. <b>IAudioStreamSample</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAudioStreamSample</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/austream/nf-austream-iaudiostreamsample-getaudiodata">GetAudioData</a>
</td>
<td align="left" width="63%">
Retrieves the address of a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/austream/nn-austream-iaudiodata">IAudioData</a> object associated with the sample.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmstream/nn-mmstream-istreamsample">IStreamSample</a>
 

 

