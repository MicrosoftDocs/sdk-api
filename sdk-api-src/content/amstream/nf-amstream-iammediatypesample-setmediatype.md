---
UID: NF:amstream.IAMMediaTypeSample.SetMediaType
title: IAMMediaTypeSample::SetMediaType (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The SetMediaType method sets the media type for the sample.
helpviewer_keywords: ["IAMMediaTypeSample interface [DirectShow]","SetMediaType method","IAMMediaTypeSample.SetMediaType","IAMMediaTypeSample::SetMediaType","IAMMediaTypeSampleSetMediaType","SetMediaType","SetMediaType method [DirectShow]","SetMediaType method [DirectShow]","IAMMediaTypeSample interface","amstream/IAMMediaTypeSample::SetMediaType","dshow.iammediatypesample_setmediatype"]
old-location: dshow\iammediatypesample_setmediatype.htm
tech.root: dshow
ms.assetid: 13c065b4-9a46-42bd-aef9-dd2a87a355df
ms.date: 4/26/2023
ms.keywords: IAMMediaTypeSample interface [DirectShow],SetMediaType method, IAMMediaTypeSample.SetMediaType, IAMMediaTypeSample::SetMediaType, IAMMediaTypeSampleSetMediaType, SetMediaType, SetMediaType method [DirectShow], SetMediaType method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::SetMediaType, dshow.iammediatypesample_setmediatype
req.header: amstream.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMMediaTypeSample::SetMediaType
 - amstream/IAMMediaTypeSample::SetMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaTypeSample.SetMediaType
---

# IAMMediaTypeSample::SetMediaType


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetMediaType</code> method sets the media type for the sample.

## -parameters

### -param pMediaType

Pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure that describes the media type.

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
Insufficient memory.

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

## -see-also

<a href="/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>