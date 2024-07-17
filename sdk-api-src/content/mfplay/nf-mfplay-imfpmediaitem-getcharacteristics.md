---
UID: NF:mfplay.IMFPMediaItem.GetCharacteristics
title: IMFPMediaItem::GetCharacteristics (mfplay.h)
description: Gets various flags that describe the media item.
helpviewer_keywords: ["GetCharacteristics","GetCharacteristics method [Media Foundation]","GetCharacteristics method [Media Foundation]","IMFPMediaItem interface","IMFPMediaItem interface [Media Foundation]","GetCharacteristics method","IMFPMediaItem.GetCharacteristics","IMFPMediaItem::GetCharacteristics","mf.imfpmediaitem_getcharacteristics","mfplay/IMFPMediaItem::GetCharacteristics"]
old-location: mf\imfpmediaitem_getcharacteristics.htm
tech.root: mfarchive
archived: true
ms.assetid: 9fe65644-c7a0-4af5-9765-f933215f5f83
ms.date: 12/05/2018
ms.keywords: GetCharacteristics, GetCharacteristics method [Media Foundation], GetCharacteristics method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetCharacteristics method, IMFPMediaItem.GetCharacteristics, IMFPMediaItem::GetCharacteristics, mf.imfpmediaitem_getcharacteristics, mfplay/IMFPMediaItem::GetCharacteristics
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
 - IMFPMediaItem::GetCharacteristics
 - mfplay/IMFPMediaItem::GetCharacteristics
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
 - IMFPMediaItem.GetCharacteristics
---

# IMFPMediaItem::GetCharacteristics


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Gets various flags that describe the media item.

## -parameters

### -param pCharacteristics [out]

Receives a bitwise <b>OR</b> of flags from the <a href="/windows/win32/api/mfplay/ne-mfplay-_mfp_mediaitem_characteristics">_MFP_MEDIAITEM_CHARACTERISTICS</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>