---
UID: NF:mfidl.IMFClockStateSink.OnClockPause
title: IMFClockStateSink::OnClockPause
author: windows-driver-content
description: Called when the presentation clock pauses.
old-location: mf\imfclockstatesink_onclockpause.htm
old-project: medfound
ms.assetid: d4eb1ddf-2eea-48e2-946a-4ea20be8cc8f
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IMFClockStateSink interface [Media Foundation],OnClockPause method, IMFClockStateSink.OnClockPause, IMFClockStateSink::OnClockPause, OnClockPause, OnClockPause method [Media Foundation], OnClockPause method [Media Foundation],IMFClockStateSink interface, d4eb1ddf-2eea-48e2-946a-4ea20be8cc8f, mf.imfclockstatesink_onclockpause, mfidl/IMFClockStateSink::OnClockPause
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFClockStateSink.OnClockPause
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFClockStateSink::OnClockPause


## -description



          Called when the presentation clock pauses.
        


## -parameters




### -param hnsSystemTime [in]


            The system time when the clock was paused, in 100-nanosecond units.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When the presentation clock's <a href="https://msdn.microsoft.com/2eddc9a9-e3a6-46c4-83c6-446b6a7a64b0">IMFPresentationClock::Pause</a> method is called, the clock notifies the presentation time source by calling the time source's <b>OnClockPause</b> method. This call occurs synchronously within the <b>Pause</b> method. If the time source returns an error from <b>OnClockPause</b>, the presentation clock's <b>Pause</b> method returns an error and the state change does not take place.

For any object that is not the presentation time source, the <b>OnClockPause</b> method is called asynchronously, after the state change is completed. In that case, the return value from this method is ignored.




## -see-also




<a href="https://msdn.microsoft.com/9aa0d2cd-a687-4b3a-834d-ccc8d3a03196">IMFClockStateSink</a>



<a href="https://msdn.microsoft.com/9273ff1f-382e-4c58-b571-4852545915b3">MFTIME</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

