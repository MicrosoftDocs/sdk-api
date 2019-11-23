---
UID: NN:mfspatialaudio.IMFSpatialAudioObjectBuffer
title: IMFSpatialAudioObjectBuffer (mfspatialaudio.h)

description: Represents a section of audio data with associated positional and rendering metadata. Spatial audio objects are stored in IMFSpatialAudioSample instances, and allow passing of spatial audio information between Media Foundation components.
old-location: mf\imfspatialaudioobjectbuffer.htm
tech.root: medfound
ms.assetid: 61E9BC6A-2120-4874-9053-E1D232DF1CCA

ms.date: 12/05/2018
ms.keywords: IMFSpatialAudioObjectBuffer, IMFSpatialAudioObjectBuffer interface [Media Foundation], IMFSpatialAudioObjectBuffer interface [Media Foundation],described, mf.imfspatialaudioobjectbuffer, mfspatialaudio/IMFSpatialAudioObjectBuffer
ms.topic: interface
f1_keywords: 
 - "mfspatialaudio/IMFSpatialAudioObjectBuffer"
dev_langs:
 - c++
req.header: mfspatialaudio.h
req.include-header: Mfobjects.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfobjects.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.lib
 - mfobjects.dll
api_name:
 - IMFSpatialAudioObjectBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSpatialAudioObjectBuffer interface


## -description


Represents a section of audio data with
associated positional and rendering metadata.  Spatial audio objects are stored in <a href="https://docs.microsoft.com/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample">IMFSpatialAudioSample</a> instances, and allow passing of 
spatial audio information between Media Foundation components.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSpatialAudioObjectBuffer</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a>. <b>IMFSpatialAudioObjectBuffer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSpatialAudioObjectBuffer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfspatialaudio/nf-mfspatialaudio-imfspatialaudioobjectbuffer-getid">GetID</a>
</td>
<td align="left" width="63%">
Returns the unique, unsigned 32-bit ID of the spatial audio object represented by the buffer.
    If <a href="https://docs.microsoft.com/windows/desktop/api/mfspatialaudio/nf-mfspatialaudio-imfspatialaudioobjectbuffer-setid">SetID</a> method was not previously called, this method returns the invalid object ID, -1 
    (0xffffffff).  The invalid ID indicates that the object buffer is unused and
    contains invalid data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfspatialaudio/nf-mfspatialaudio-imfspatialaudioobjectbuffer-getmetadataitems">GetMetadataItems</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to a buffer that may 
    contain spatial audio metadata.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfspatialaudio/nf-mfspatialaudio-imfspatialaudioobjectbuffer-gettype">GetType</a>
</td>
<td align="left" width="63%">
Gets the type of the spatial audio object represented by the buffer. If <a href="https://docs.microsoft.com/windows/desktop/api/mfspatialaudio/nf-mfspatialaudio-imfspatialaudioobjectbuffer-settype">SetType</a> has not been called previously, this method returns the default value of <b>AudioObjectType_None</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfspatialaudio/nf-mfspatialaudio-imfspatialaudioobjectbuffer-setid">SetID</a>
</td>
<td align="left" width="63%">
Sets the ID of the spatial audio object represented by the buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfspatialaudio/nf-mfspatialaudio-imfspatialaudioobjectbuffer-settype">SetType</a>
</td>
<td align="left" width="63%">
Sets the type of the spatial audio object represented by the buffer.

</td>
</tr>
</table> 


## -remarks



To get the audio data contained in the spatial audio object, use the    <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock">IMFMediaBuffer::Lock</a> and <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock">IMFMediaBuffer::Unlock</a> methods.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a>
 

 

