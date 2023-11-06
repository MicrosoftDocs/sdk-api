---
UID: NF:qnetwork.IAMExtendedSeeking.get_CurrentMarker
title: IAMExtendedSeeking::get_CurrentMarker (qnetwork.h)
description: The get_CurrentMarker method retrieves the current marker.
helpviewer_keywords: ["IAMExtendedSeeking interface [DirectShow]","get_CurrentMarker method","IAMExtendedSeeking.get_CurrentMarker","IAMExtendedSeeking::get_CurrentMarker","IAMExtendedSeekingget_CurrentMarker","dshow.iamextendedseeking_get_currentmarker","get_CurrentMarker","get_CurrentMarker method [DirectShow]","get_CurrentMarker method [DirectShow]","IAMExtendedSeeking interface","qnetwork/IAMExtendedSeeking::get_CurrentMarker"]
old-location: dshow\iamextendedseeking_get_currentmarker.htm
tech.root: dshow
ms.assetid: dd2d2054-0f92-4ba5-8913-24278e01775e
ms.date: 4/26/2023
ms.keywords: IAMExtendedSeeking interface [DirectShow],get_CurrentMarker method, IAMExtendedSeeking.get_CurrentMarker, IAMExtendedSeeking::get_CurrentMarker, IAMExtendedSeekingget_CurrentMarker, dshow.iamextendedseeking_get_currentmarker, get_CurrentMarker, get_CurrentMarker method [DirectShow], get_CurrentMarker method [DirectShow],IAMExtendedSeeking interface, qnetwork/IAMExtendedSeeking::get_CurrentMarker
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
 - IAMExtendedSeeking::get_CurrentMarker
 - qnetwork/IAMExtendedSeeking::get_CurrentMarker
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
 - IAMExtendedSeeking.get_CurrentMarker
---

# IAMExtendedSeeking::get_CurrentMarker


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_CurrentMarker</code> method retrieves the current marker.

## -parameters

### -param pCurrentMarker [out]

Pointer to a variable that receives the current marker.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamextendedseeking">IAMExtendedSeeking Interface</a>