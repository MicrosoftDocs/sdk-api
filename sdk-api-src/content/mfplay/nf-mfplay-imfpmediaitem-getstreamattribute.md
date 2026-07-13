---
UID: NF:mfplay.IMFPMediaItem.GetStreamAttribute
title: IMFPMediaItem::GetStreamAttribute (mfplay.h)
description: Queries the media item for a stream attribute.
helpviewer_keywords: ["GetStreamAttribute","GetStreamAttribute method [Media Foundation]","GetStreamAttribute method [Media Foundation]","IMFPMediaItem interface","IMFPMediaItem interface [Media Foundation]","GetStreamAttribute method","IMFPMediaItem.GetStreamAttribute","IMFPMediaItem::GetStreamAttribute","mf.imfpmediaitem_getstreamattribute","mfplay/IMFPMediaItem::GetStreamAttribute"]
old-location: mf\imfpmediaitem_getstreamattribute.htm
tech.root: mfarchive
archived: true
ms.assetid: 8c40ce33-2077-4e7b-8a1c-c080e82df078
ms.date: 12/05/2018
ms.keywords: GetStreamAttribute, GetStreamAttribute method [Media Foundation], GetStreamAttribute method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetStreamAttribute method, IMFPMediaItem.GetStreamAttribute, IMFPMediaItem::GetStreamAttribute, mf.imfpmediaitem_getstreamattribute, mfplay/IMFPMediaItem::GetStreamAttribute
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IMFPMediaItem::GetStreamAttribute
 - mfplay/IMFPMediaItem::GetStreamAttribute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplay.h
api_name:
 - IMFPMediaItem.GetStreamAttribute
---

# IMFPMediaItem::GetStreamAttribute


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Queries the media item for a stream attribute.

## -parameters

### -param dwStreamIndex [in]

Zero-based index of the stream. To get the number of streams, call <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getnumberofstreams">IMFPMediaItem::GetNumberOfStreams</a>.

### -param guidMFAttribute [in]

GUID that identifies the attribute value to query. Possible values are listed in the following topics:

<ul>
<li>
<a href="/windows/desktop/medfound/stream-descriptor-attributes">Stream Descriptor Attributes</a>
</li>
<li>
<a href="/windows/desktop/medfound/media-type-attributes">Media Type Attributes</a>
</li>
</ul>

### -param pvValue [out]

Pointer to a <b>PROPVARIANT</b> that receives the value. The method fills the <b>PROPVARIANT</b> with a copy of the stored value. Call <b>PropVariantClear</b> to free the memory allocated by this method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Stream attributes describe an individual stream (audio, video, or other) within the presentation. To get an attribute that applies to the entire presentation, call <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getpresentationattribute">IMFPMediaItem::GetPresentationAttribute</a>.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>