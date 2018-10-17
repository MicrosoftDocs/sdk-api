---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetTimelineMarkerTimer
title: IMFMediaEngineEx::SetTimelineMarkerTimer
author: windows-sdk-content
description: Specifies a presentation time when the Media Engine will send a marker event.
old-location: mf\imfmediaengineex_settimelinemarkertimer.htm
tech.root: medfound
ms.assetid: 2FD65E4A-C70A-4CB4-9038-3A8B791E251C
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],SetTimelineMarkerTimer method, IMFMediaEngineEx.SetTimelineMarkerTimer, IMFMediaEngineEx::SetTimelineMarkerTimer, SetTimelineMarkerTimer, SetTimelineMarkerTimer method [Media Foundation], SetTimelineMarkerTimer method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_settimelinemarkertimer, mfmediaengine/IMFMediaEngineEx::SetTimelineMarkerTimer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx.SetTimelineMarkerTimer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineEx::SetTimelineMarkerTimer


## -description


Specifies a presentation time when the Media Engine will send a marker event.


## -parameters




### -param timeToFire [in]

The presentation time for the marker event, in seconds.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When playback reaches the time specified by <i>timeToFire</i>, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_TIMELINE_MARKER</b> event through the <a href="https://msdn.microsoft.com/F6B9E025-53C4-4459-9EC4-EA228065FAD3">IMFMediaEngineNotify::EventNotify</a> method. Calling this method cancels any previous marker that is still pending. 

If the application seeks past the marker point, the Media Engine cancels the marker and does not send the event.

During  forward playback, set <i>timeToFire</i> to a value greater than the current playback position. During reverse playback, set <i>timeToFire</i> to a value less than the playback position.

To cancel a marker, call <a href="https://msdn.microsoft.com/AC295919-747B-445D-8C74-E648A612C0BF">IMFMediaEngineEx::CancelTimelineMarkerTimer</a>.




## -see-also




<a href="https://msdn.microsoft.com/EE3591FD-4FE8-4F20-A4E2-52C896229571">IMFMediaEngineEx</a>
 

 

