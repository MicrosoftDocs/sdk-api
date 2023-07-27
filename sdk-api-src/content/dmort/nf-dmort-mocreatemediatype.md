---
UID: NF:dmort.MoCreateMediaType
title: MoCreateMediaType function (dmort.h)
description: The MoCreateMediaType function allocates a new media type structure.
helpviewer_keywords: ["MoCreateMediaType","MoCreateMediaType function [DirectShow]","dmort/MoCreateMediaType","dshow.mocreatemediatype"]
old-location: dshow\mocreatemediatype.htm
tech.root: dshow
ms.assetid: f67b04b5-163e-4793-8df0-10a4b2be5025
ms.date: 4/26/2023
ms.keywords: MoCreateMediaType, MoCreateMediaType function [DirectShow], dmort/MoCreateMediaType, dshow.mocreatemediatype
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
 - MoCreateMediaType
 - dmort/MoCreateMediaType
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
 - MoCreateMediaType
---

# MoCreateMediaType function


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>MoCreateMediaType</b> function allocates a new media type structure.

## -parameters

### -param ppmt

Receives a pointer to an allocated <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type">DMO_MEDIA_TYPE</a> structure.

### -param cbFormat

Number of bytes to allocate for the format block. Can be zero.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory

</td>
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

This function allocates a new <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type">DMO_MEDIA_TYPE</a> structure on the heap. It also allocates memory for the format block. The caller must delete the structure by calling the <a href="/windows/desktop/api/dmort/nf-dmort-modeletemediatype">MoDeleteMediaType</a> function.

Internally, this function calls <a href="/windows/desktop/api/dmort/nf-dmort-moinitmediatype">MoInitMediaType</a> to allocate the format block.