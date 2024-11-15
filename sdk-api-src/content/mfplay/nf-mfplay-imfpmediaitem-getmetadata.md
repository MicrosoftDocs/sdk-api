---
UID: NF:mfplay.IMFPMediaItem.GetMetadata
title: IMFPMediaItem::GetMetadata (mfplay.h)
description: Gets a property store that contains metadata for the source, such as author or title.
helpviewer_keywords: ["GetMetadata","GetMetadata method [Media Foundation]","GetMetadata method [Media Foundation]","IMFPMediaItem interface","IMFPMediaItem interface [Media Foundation]","GetMetadata method","IMFPMediaItem.GetMetadata","IMFPMediaItem::GetMetadata","mf.imfpmediaitem_getmetadata","mfplay/IMFPMediaItem::GetMetadata"]
old-location: mf\imfpmediaitem_getmetadata.htm
tech.root: mfarchive
archived: true
ms.assetid: 212d468f-de5e-4a55-aaa4-ed487bbf6a00
ms.date: 12/05/2018
ms.keywords: GetMetadata, GetMetadata method [Media Foundation], GetMetadata method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetMetadata method, IMFPMediaItem.GetMetadata, IMFPMediaItem::GetMetadata, mf.imfpmediaitem_getmetadata, mfplay/IMFPMediaItem::GetMetadata
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
 - IMFPMediaItem::GetMetadata
 - mfplay/IMFPMediaItem::GetMetadata
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
 - IMFPMediaItem.GetMetadata
---

# IMFPMediaItem::GetMetadata


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Gets a property store that contains metadata for the source, such as author or title.

## -parameters

### -param ppMetadataStore [out]

Receives a pointer to the <b>IPropertyStore</b> interface of a read-only property store. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>