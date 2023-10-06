---
UID: NF:dmort.MoDeleteMediaType
title: MoDeleteMediaType function (dmort.h)
description: The MoDeleteMediaType function deletes a media type structure that was previously allocated.
helpviewer_keywords: ["MoDeleteMediaType","MoDeleteMediaType function [DirectShow]","dmort/MoDeleteMediaType","dshow.modeletemediatype"]
old-location: dshow\modeletemediatype.htm
tech.root: dshow
ms.assetid: adbfe1e1-e956-48de-9ed1-9f8f4c66ff1c
ms.date: 4/26/2023
ms.keywords: MoDeleteMediaType, MoDeleteMediaType function [DirectShow], dmort/MoDeleteMediaType, dshow.modeletemediatype
req.header: dmort.h
req.include-header: Dmo.h
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
req.lib: Msdmo.lib
req.dll: Msdmo.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MoDeleteMediaType
 - dmort/MoDeleteMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdmo.dll
api_name:
 - MoDeleteMediaType
---

# MoDeleteMediaType function


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>MoDeleteMediaType</b> function deletes a media type structure that was previously allocated.

## -parameters

### -param pmt

Pointer to an initialized <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type">DMO_MEDIA_TYPE</a> structure.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -remarks

Call this function to free a <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type">DMO_MEDIA_TYPE</a> structure that was allocated with the <a href="/windows/desktop/api/dmort/nf-dmort-mocreatemediatype">MoCreateMediaType</a> function.

Internally, this function calls <a href="/windows/desktop/api/dmort/nf-dmort-mofreemediatype">MoFreeMediaType</a> to free the format block.