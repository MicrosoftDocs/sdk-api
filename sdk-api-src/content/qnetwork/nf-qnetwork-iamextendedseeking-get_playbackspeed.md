---
UID: NF:qnetwork.IAMExtendedSeeking.get_PlaybackSpeed
title: IAMExtendedSeeking::get_PlaybackSpeed (qnetwork.h)
description: The get_PlaybackSpeed method retrieves the playback speed.
helpviewer_keywords: ["IAMExtendedSeeking interface [DirectShow]","get_PlaybackSpeed method","IAMExtendedSeeking.get_PlaybackSpeed","IAMExtendedSeeking::get_PlaybackSpeed","IAMExtendedSeekingget_PlaybackSpeed","dshow.iamextendedseeking_get_playbackspeed","get_PlaybackSpeed","get_PlaybackSpeed method [DirectShow]","get_PlaybackSpeed method [DirectShow]","IAMExtendedSeeking interface","qnetwork/IAMExtendedSeeking::get_PlaybackSpeed"]
old-location: dshow\iamextendedseeking_get_playbackspeed.htm
tech.root: dshow
ms.assetid: a92309fb-185a-4d6c-81c2-9613634c7170
ms.date: 4/26/2023
ms.keywords: IAMExtendedSeeking interface [DirectShow],get_PlaybackSpeed method, IAMExtendedSeeking.get_PlaybackSpeed, IAMExtendedSeeking::get_PlaybackSpeed, IAMExtendedSeekingget_PlaybackSpeed, dshow.iamextendedseeking_get_playbackspeed, get_PlaybackSpeed, get_PlaybackSpeed method [DirectShow], get_PlaybackSpeed method [DirectShow],IAMExtendedSeeking interface, qnetwork/IAMExtendedSeeking::get_PlaybackSpeed
req.header: qnetwork.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMExtendedSeeking::get_PlaybackSpeed
 - qnetwork/IAMExtendedSeeking::get_PlaybackSpeed
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMExtendedSeeking.get_PlaybackSpeed
---

# IAMExtendedSeeking::get_PlaybackSpeed


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_PlaybackSpeed</code> method retrieves the playback speed.

## -parameters

### -param pSpeed [out]

Pointer to a variable that receives the playback speed.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamextendedseeking">IAMExtendedSeeking Interface</a>



<a href="/windows/desktop/api/qnetwork/nf-qnetwork-iamextendedseeking-put_playbackspeed">IAMExtendedSeeking::put_PlaybackSpeed</a>