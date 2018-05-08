---
UID: NN:austream.IAudioStreamSample
title: IAudioStreamSample
author: windows-driver-content
description: Note  This interface is deprecated.
old-location: dshow\iaudiostreamsample.htm
old-project: DirectShow
ms.assetid: 53deec43-30ca-472e-9a82-750049686d2a
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IAudioStreamSample, IAudioStreamSample interface [DirectShow], IAudioStreamSample interface [DirectShow],described, IAudioStreamSampleInterface, austream/IAudioStreamSample, dshow.iaudiostreamsample
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: AUDIO_STREAM_CATEGORY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	austream.h
api_name:
-	IAudioStreamSample
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioStreamSample interface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>IAudioStreamSample</code> interface retrieves information from the underlying <a href="https://msdn.microsoft.com/8b253715-a294-4e95-b730-e6efe7f895af">IAudioData</a> data objects.

For sample code that implements the audio streaming interfaces, see <a href="https://msdn.microsoft.com/3fe2996b-b4de-40ad-bd02-d850a45f3a2c">Multimedia Streaming Sample Code</a>.

Implement this interface on audio stream sample objects when they need access to an <a href="https://msdn.microsoft.com/8b253715-a294-4e95-b730-e6efe7f895af">IAudioData</a> object's data.

Use this interface when your application needs to access an <a href="https://msdn.microsoft.com/8b253715-a294-4e95-b730-e6efe7f895af">IAudioData</a> object's data for its audio stream.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAudioStreamSample</b> interface inherits from <a href="https://msdn.microsoft.com/57818d7d-3290-46f7-a3fd-8585cdd64ec3">IStreamSample</a>. <b>IAudioStreamSample</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b482e628-d4bc-461e-b529-58e891689513">GetAudioData</a>
</td>
<td align="left" width="63%">
Retrieves the address of a pointer to the <a href="https://msdn.microsoft.com/8b253715-a294-4e95-b730-e6efe7f895af">IAudioData</a> object associated with the sample.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/57818d7d-3290-46f7-a3fd-8585cdd64ec3">IStreamSample</a>
 

 

