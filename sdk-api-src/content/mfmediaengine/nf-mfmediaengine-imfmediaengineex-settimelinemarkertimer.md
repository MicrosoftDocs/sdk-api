---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

