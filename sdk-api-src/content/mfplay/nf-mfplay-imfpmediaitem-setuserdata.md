---
UID: NF:mfplay.IMFPMediaItem.SetUserData
title: IMFPMediaItem::SetUserData (mfplay.h)
description: Stores an application-defined value in the media item.
helpviewer_keywords: ["IMFPMediaItem interface [Media Foundation]","SetUserData method","IMFPMediaItem.SetUserData","IMFPMediaItem::SetUserData","SetUserData","SetUserData method [Media Foundation]","SetUserData method [Media Foundation]","IMFPMediaItem interface","mf.imfpmediaitem_setuserdata","mfplay/IMFPMediaItem::SetUserData"]
old-location: mf\imfpmediaitem_setuserdata.htm
tech.root: mfarchive
archived: true
ms.assetid: 17a10427-f13a-494c-bb68-a7722e8d9b6e
ms.date: 12/05/2018
ms.keywords: IMFPMediaItem interface [Media Foundation],SetUserData method, IMFPMediaItem.SetUserData, IMFPMediaItem::SetUserData, SetUserData, SetUserData method [Media Foundation], SetUserData method [Media Foundation],IMFPMediaItem interface, mf.imfpmediaitem_setuserdata, mfplay/IMFPMediaItem::SetUserData
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
 - IMFPMediaItem::SetUserData
 - mfplay/IMFPMediaItem::SetUserData
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
 - IMFPMediaItem.SetUserData
---

# IMFPMediaItem::SetUserData


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Stores an application-defined value in the media item.

## -parameters

### -param dwUserData [in]

The application-defined value.

## -returns

This method can return one of these values.

## -remarks

This method can be called after the player object is shut down.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>