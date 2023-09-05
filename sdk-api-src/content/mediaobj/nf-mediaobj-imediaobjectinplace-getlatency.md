---
UID: NF:mediaobj.IMediaObjectInPlace.GetLatency
title: IMediaObjectInPlace::GetLatency (mediaobj.h)
description: The GetLatency method retrieves the latency introduced by this DMO.
helpviewer_keywords: ["GetLatency","GetLatency method [DirectShow]","GetLatency method [DirectShow]","IMediaObjectInPlace interface","IMediaObjectInPlace interface [DirectShow]","GetLatency method","IMediaObjectInPlace.GetLatency","IMediaObjectInPlace::GetLatency","IMediaObjectInPlaceGetLatency","dshow.imediaobjectinplace_getlatency","mediaobj/IMediaObjectInPlace::GetLatency"]
old-location: dshow\imediaobjectinplace_getlatency.htm
tech.root: dshow
ms.assetid: f6ed4824-bc18-4a12-82d3-d68e98f6d964
ms.date: 4/26/2023
ms.keywords: GetLatency, GetLatency method [DirectShow], GetLatency method [DirectShow],IMediaObjectInPlace interface, IMediaObjectInPlace interface [DirectShow],GetLatency method, IMediaObjectInPlace.GetLatency, IMediaObjectInPlace::GetLatency, IMediaObjectInPlaceGetLatency, dshow.imediaobjectinplace_getlatency, mediaobj/IMediaObjectInPlace::GetLatency
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
 - IMediaObjectInPlace::GetLatency
 - mediaobj/IMediaObjectInPlace::GetLatency
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
 - IMediaObjectInPlace.GetLatency
---

# IMediaObjectInPlace::GetLatency


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetLatency</code> method retrieves the latency introduced by this DMO.

## -parameters

### -param pLatencyTime [out]

Pointer to a variable that receives the latency, in 100-nanosecond units.

## -returns

Returns S_OK if successful. Otherwise, returns an <b>HRESULT</b> value indicating the cause of the error.

## -remarks

This method returns the average time required to process each buffer. This value usually depends on factors in the run-time environment, such as the processor speed and the CPU load. One possible way to implement this method is for the DMO to keep a running average based on historical data.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace">IMediaObjectInPlace Interface</a>