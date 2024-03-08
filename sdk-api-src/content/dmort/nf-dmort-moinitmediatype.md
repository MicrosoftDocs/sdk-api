---
UID: NF:dmort.MoInitMediaType
title: MoInitMediaType function (dmort.h)
description: The MoInitMediaType function initializes a media type structure.
helpviewer_keywords: ["MoInitMediaType","MoInitMediaType function [DirectShow]","dmort/MoInitMediaType","dshow.moinitmediatype"]
old-location: dshow\moinitmediatype.htm
tech.root: dshow
ms.assetid: 526ad3c6-a002-4b79-9712-47ea9ce321ba
ms.date: 4/26/2023
ms.keywords: MoInitMediaType, MoInitMediaType function [DirectShow], dmort/MoInitMediaType, dshow.moinitmediatype
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
 - MoInitMediaType
 - dmort/MoInitMediaType
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
 - MoInitMediaType
---

# MoInitMediaType function


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>MoInitMediaType</b> function initializes a media type structure.

## -parameters

### -param pmt

Pointer to an uninitialized <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type">DMO_MEDIA_TYPE</a> structure allocated by the caller.

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

This function allocates the format block for a <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type">DMO_MEDIA_TYPE</a> structure. The format block is allocated on the heap. The allocated memory is not initialized. The caller must free the format block by calling the <a href="/windows/desktop/api/dmort/nf-dmort-mofreemediatype">MoFreeMediaType</a> function. 



This function also sets the <b>cbFormat</b> and <b>pbFormat</b> members of the <a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type">DMO_MEDIA_TYPE</a> structure.