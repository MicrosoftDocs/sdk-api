---
UID: NF:qnetwork.IAMExtendedSeeking.put_PlaybackSpeed
title: IAMExtendedSeeking::put_PlaybackSpeed (qnetwork.h)
description: The put_PlaybackSpeed method specifies the playback speed.
helpviewer_keywords: ["IAMExtendedSeeking interface [DirectShow]","put_PlaybackSpeed method","IAMExtendedSeeking.put_PlaybackSpeed","IAMExtendedSeeking::put_PlaybackSpeed","IAMExtendedSeekingput_PlaybackSpeed","dshow.iamextendedseeking_put_playbackspeed","put_PlaybackSpeed","put_PlaybackSpeed method [DirectShow]","put_PlaybackSpeed method [DirectShow]","IAMExtendedSeeking interface","qnetwork/IAMExtendedSeeking::put_PlaybackSpeed"]
old-location: dshow\iamextendedseeking_put_playbackspeed.htm
tech.root: dshow
ms.assetid: c4f958eb-b573-44e4-94e1-5ac422dd1a99
ms.date: 12/05/2018
ms.keywords: IAMExtendedSeeking interface [DirectShow],put_PlaybackSpeed method, IAMExtendedSeeking.put_PlaybackSpeed, IAMExtendedSeeking::put_PlaybackSpeed, IAMExtendedSeekingput_PlaybackSpeed, dshow.iamextendedseeking_put_playbackspeed, put_PlaybackSpeed, put_PlaybackSpeed method [DirectShow], put_PlaybackSpeed method [DirectShow],IAMExtendedSeeking interface, qnetwork/IAMExtendedSeeking::put_PlaybackSpeed
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
 - IAMExtendedSeeking::put_PlaybackSpeed
 - qnetwork/IAMExtendedSeeking::put_PlaybackSpeed
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
 - IAMExtendedSeeking.put_PlaybackSpeed
---

# IAMExtendedSeeking::put_PlaybackSpeed


## -description

The <code>put_PlaybackSpeed</code> method specifies the playback speed.

## -parameters

### -param Speed [in]

Specifies the playback speed. The value may be positive or negative, but not zero.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamextendedseeking">IAMExtendedSeeking Interface</a>



<a href="/windows/desktop/api/qnetwork/nf-qnetwork-iamextendedseeking-get_playbackspeed">IAMExtendedSeeking::get_PlaybackSpeed</a>