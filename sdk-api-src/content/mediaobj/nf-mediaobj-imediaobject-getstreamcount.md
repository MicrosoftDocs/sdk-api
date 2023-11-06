---
UID: NF:mediaobj.IMediaObject.GetStreamCount
title: IMediaObject::GetStreamCount (mediaobj.h)
description: The GetStreamCount method retrieves the number of input and output streams.
helpviewer_keywords: ["GetStreamCount","GetStreamCount method [DirectShow]","GetStreamCount method [DirectShow]","IMediaObject interface","IMediaObject interface [DirectShow]","GetStreamCount method","IMediaObject.GetStreamCount","IMediaObject::GetStreamCount","IMediaObjectGetStreamCount","dshow.imediaobject_getstreamcount","mediaobj/IMediaObject::GetStreamCount"]
old-location: dshow\imediaobject_getstreamcount.htm
tech.root: dshow
ms.assetid: 05c28b44-6b92-418b-bb3f-889e59f4e0c1
ms.date: 4/26/2023
ms.keywords: GetStreamCount, GetStreamCount method [DirectShow], GetStreamCount method [DirectShow],IMediaObject interface, IMediaObject interface [DirectShow],GetStreamCount method, IMediaObject.GetStreamCount, IMediaObject::GetStreamCount, IMediaObjectGetStreamCount, dshow.imediaobject_getstreamcount, mediaobj/IMediaObject::GetStreamCount
req.header: mediaobj.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaObject::GetStreamCount
 - mediaobj/IMediaObject::GetStreamCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObject.GetStreamCount
---

# IMediaObject::GetStreamCount


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetStreamCount</code> method retrieves the number of input and output streams.

## -parameters

### -param pcInputStreams [out]

Pointer to a variable that receives the number of input streams. Cannot be <b>NULL</b>.

### -param pcOutputStreams [out]

Pointer to a variable that receives the number of output streams. Cannot be <b>NULL</b>.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those in the following table.

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

The DMO might have zero input streams or zero output streams. The number of streams does not change; a DMO cannot dynamically add or remove streams.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject Interface</a>