---
UID: NF:mfidl.IMFClockStateSink.OnClockStart
title: IMFClockStateSink::OnClockStart method
author: windows-driver-content
description: Called when the presentation clock starts.
old-location: mf\imfclockstatesink_onclockstart.htm
old-project: medfound
ms.assetid: 1a696ffc-b8e6-4ef9-b980-35bfbd3d4128
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: 1a696ffc-b8e6-4ef9-b980-35bfbd3d4128, IMFClockStateSink, IMFClockStateSink interface [Media Foundation], OnClockStart method, IMFClockStateSink::OnClockStart, OnClockStart method [Media Foundation], OnClockStart method [Media Foundation], IMFClockStateSink interface, OnClockStart,IMFClockStateSink.OnClockStart, mf.imfclockstatesink_onclockstart, mfidl/IMFClockStateSink::OnClockStart
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFClockStateSink.OnClockStart
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFClockStateSink::OnClockStart method


## -description



          Called when the presentation clock starts.
        


## -parameters




### -param hnsSystemTime [in]


            The system time when the clock started, in 100-nanosecond units.
          


### -param llClockStartOffset [in]


            The new starting time for the clock, in 100-nanosecond units. This parameter can also equal <b>PRESENTATION_CURRENT_POSITION</b>, indicating the clock has started or restarted from its current position.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called whe the presentation clock's <a href="https://msdn.microsoft.com/ba5986d1-9c94-4747-a221-43d0583f1fed">IMFPresentationClock::Start</a> method is called, with the following exception: If the clock is paused and <b>Start</b> is called with the value <b>PRESENTATION_CURRENT_POSITION</b>, <a href="https://msdn.microsoft.com/55973dfa-59b9-4105-9706-5d5497ad2818">IMFClockStateSink::OnClockRestart</a> is called instead of <b>OnClockStart</b>.

The clock notifies the presentation time source by calling the time source's <b>OnClockStart</b> method. This call occurs synchronously within the <a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a> method. If the time source returns an error from <b>OnClockStart</b>, the presentation clock's <b>Start</b> method returns an error and the state change does not take place.

For any object that is not the presentation time source, the <b>OnClockStart</b> method is called asynchronously, after the state change is completed. In that case, the return value from this method is ignored.

The value given in <i>llClockStartOffset</i> is the presentation time when the clock starts, so it is relative to the start of the presentation. Media sinks should not render any data with a presentation time earlier than <i>llClockStartOffSet</i>. If a sample straddles the offset—that is, if the offset falls between the sample's start and stop times—the sink should either trim the sample so that only data after <i>llClockStartOffset</i> is rendered, or else simply drop the sample.




## -see-also




<a href="https://msdn.microsoft.com/9aa0d2cd-a687-4b3a-834d-ccc8d3a03196">IMFClockStateSink</a>



<a href="https://msdn.microsoft.com/9273ff1f-382e-4c58-b571-4852545915b3">MFTIME</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

