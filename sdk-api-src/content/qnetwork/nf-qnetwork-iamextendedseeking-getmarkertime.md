---
UID: NF:qnetwork.IAMExtendedSeeking.GetMarkerTime
title: IAMExtendedSeeking::GetMarkerTime (qnetwork.h)
description: The GetMarkerTime method retrieves the presentation time associated with the specified marker.
helpviewer_keywords: ["GetMarkerTime","GetMarkerTime method [DirectShow]","GetMarkerTime method [DirectShow]","IAMExtendedSeeking interface","IAMExtendedSeeking interface [DirectShow]","GetMarkerTime method","IAMExtendedSeeking.GetMarkerTime","IAMExtendedSeeking::GetMarkerTime","IAMExtendedSeekingGetMarkerTime","dshow.iamextendedseeking_getmarkertime","qnetwork/IAMExtendedSeeking::GetMarkerTime"]
old-location: dshow\iamextendedseeking_getmarkertime.htm
tech.root: dshow
ms.assetid: 719e87c5-7d38-4b02-8342-055e42405511
ms.date: 4/26/2023
ms.keywords: GetMarkerTime, GetMarkerTime method [DirectShow], GetMarkerTime method [DirectShow],IAMExtendedSeeking interface, IAMExtendedSeeking interface [DirectShow],GetMarkerTime method, IAMExtendedSeeking.GetMarkerTime, IAMExtendedSeeking::GetMarkerTime, IAMExtendedSeekingGetMarkerTime, dshow.iamextendedseeking_getmarkertime, qnetwork/IAMExtendedSeeking::GetMarkerTime
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
 - IAMExtendedSeeking::GetMarkerTime
 - qnetwork/IAMExtendedSeeking::GetMarkerTime
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
 - IAMExtendedSeeking.GetMarkerTime
---

# IAMExtendedSeeking::GetMarkerTime


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetMarkerTime</b> method retrieves the presentation time associated with the specified marker.

## -parameters

### -param MarkerNum [in]

Specifies the marker number.

### -param pMarkerTime [out]

Pointer to a variable that receives the marker time.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamextendedseeking">IAMExtendedSeeking Interface</a>



<a href="/windows/desktop/api/qnetwork/nf-qnetwork-iamextendedseeking-getmarkername">IAMExtendedSeeking::GetMarkerName</a>