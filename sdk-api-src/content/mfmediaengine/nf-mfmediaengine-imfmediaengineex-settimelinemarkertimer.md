---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetTimelineMarkerTimer
title: IMFMediaEngineEx::SetTimelineMarkerTimer (mfmediaengine.h)
description: Specifies a presentation time when the Media Engine will send a marker event.
helpviewer_keywords: ["IMFMediaEngineEx interface [Media Foundation]","SetTimelineMarkerTimer method","IMFMediaEngineEx.SetTimelineMarkerTimer","IMFMediaEngineEx::SetTimelineMarkerTimer","SetTimelineMarkerTimer","SetTimelineMarkerTimer method [Media Foundation]","SetTimelineMarkerTimer method [Media Foundation]","IMFMediaEngineEx interface","mf.imfmediaengineex_settimelinemarkertimer","mfmediaengine/IMFMediaEngineEx::SetTimelineMarkerTimer"]
old-location: mf\imfmediaengineex_settimelinemarkertimer.htm
tech.root: mf
ms.assetid: 2FD65E4A-C70A-4CB4-9038-3A8B791E251C
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],SetTimelineMarkerTimer method, IMFMediaEngineEx.SetTimelineMarkerTimer, IMFMediaEngineEx::SetTimelineMarkerTimer, SetTimelineMarkerTimer, SetTimelineMarkerTimer method [Media Foundation], SetTimelineMarkerTimer method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_settimelinemarkertimer, mfmediaengine/IMFMediaEngineEx::SetTimelineMarkerTimer
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaEngineEx::SetTimelineMarkerTimer
 - mfmediaengine/IMFMediaEngineEx::SetTimelineMarkerTimer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx.SetTimelineMarkerTimer
---

# IMFMediaEngineEx::SetTimelineMarkerTimer


## -description

Specifies a presentation time when the Media Engine will send a marker event.

## -parameters

### -param timeToFire [in]

The presentation time for the marker event, in seconds.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When playback reaches the time specified by <i>timeToFire</i>, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_TIMELINE_MARKER</b> event through the <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginenotify-eventnotify">IMFMediaEngineNotify::EventNotify</a> method. Calling this method cancels any previous marker that is still pending. 

If the application seeks past the marker point, the Media Engine cancels the marker and does not send the event.

During  forward playback, set <i>timeToFire</i> to a value greater than the current playback position. During reverse playback, set <i>timeToFire</i> to a value less than the playback position.

To cancel a marker, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-canceltimelinemarkertimer">IMFMediaEngineEx::CancelTimelineMarkerTimer</a>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>