---
UID: NF:qnetwork.IAMExtendedSeeking.get_MarkerCount
title: IAMExtendedSeeking::get_MarkerCount (qnetwork.h)
description: The get_MarkerCount method retrieves the number of markers in the current stream.
helpviewer_keywords: ["IAMExtendedSeeking interface [DirectShow]","get_MarkerCount method","IAMExtendedSeeking.get_MarkerCount","IAMExtendedSeeking::get_MarkerCount","IAMExtendedSeekingget_MarkerCount","dshow.iamextendedseeking_get_markercount","get_MarkerCount","get_MarkerCount method [DirectShow]","get_MarkerCount method [DirectShow]","IAMExtendedSeeking interface","qnetwork/IAMExtendedSeeking::get_MarkerCount"]
old-location: dshow\iamextendedseeking_get_markercount.htm
tech.root: dshow
ms.assetid: bd9c2ca8-e5f2-409e-aaf9-d89d81d2b02d
ms.date: 4/26/2023
ms.keywords: IAMExtendedSeeking interface [DirectShow],get_MarkerCount method, IAMExtendedSeeking.get_MarkerCount, IAMExtendedSeeking::get_MarkerCount, IAMExtendedSeekingget_MarkerCount, dshow.iamextendedseeking_get_markercount, get_MarkerCount, get_MarkerCount method [DirectShow], get_MarkerCount method [DirectShow],IAMExtendedSeeking interface, qnetwork/IAMExtendedSeeking::get_MarkerCount
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
 - IAMExtendedSeeking::get_MarkerCount
 - qnetwork/IAMExtendedSeeking::get_MarkerCount
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
 - IAMExtendedSeeking.get_MarkerCount
---

# IAMExtendedSeeking::get_MarkerCount


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_MarkerCount</code> method retrieves the number of markers in the current stream.

## -parameters

### -param pMarkerCount [out]

Pointer to a variable that receives the marker count.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamextendedseeking">IAMExtendedSeeking Interface</a>