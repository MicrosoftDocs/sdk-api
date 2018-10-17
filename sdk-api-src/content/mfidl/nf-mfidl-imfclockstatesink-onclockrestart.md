---
UID: NF:mfidl.IMFClockStateSink.OnClockRestart
title: IMFClockStateSink::OnClockRestart
author: windows-sdk-content
description: Called when the presentation clock restarts from the same position while paused.
old-location: mf\imfclockstatesink_onclockrestart.htm
tech.root: medfound
ms.assetid: 55973dfa-59b9-4105-9706-5d5497ad2818
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: 55973dfa-59b9-4105-9706-5d5497ad2818, IMFClockStateSink interface [Media Foundation],OnClockRestart method, IMFClockStateSink.OnClockRestart, IMFClockStateSink::OnClockRestart, OnClockRestart, OnClockRestart method [Media Foundation], OnClockRestart method [Media Foundation],IMFClockStateSink interface, mf.imfclockstatesink_onclockrestart, mfidl/IMFClockStateSink::OnClockRestart
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFClockStateSink.OnClockRestart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFClockStateSink::OnClockRestart


## -description


Called when the presentation clock restarts from the same position while paused.
        


## -parameters




### -param hnsSystemTime [in]

The system time when the clock restarted, in 100-nanosecond units.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called if the presentation clock is paused and the <a href="https://msdn.microsoft.com/ba5986d1-9c94-4747-a221-43d0583f1fed">IMFPresentationClock::Start</a> method is called with the value <b>PRESENTATION_CURRENT_POSITION</b>.
      

The clock notifies the presentation time source by calling the time source's <b>OnClockRestart</b> method. This call occurs synchronously within the <a href="https://msdn.microsoft.com/ba5986d1-9c94-4747-a221-43d0583f1fed">Start</a> method. If the time source returns an error from <b>OnClockRestart</b>, the presentation clock's <b>Start</b> method returns an error and the state change does not take place.
      

For any object that is not the presentation time source, the <b>OnClockRestart</b> method is called asynchronously, after the state change is completed. In that case, the return value from this method is ignored.
      




## -see-also




<a href="https://msdn.microsoft.com/9aa0d2cd-a687-4b3a-834d-ccc8d3a03196">IMFClockStateSink</a>



<a href="https://msdn.microsoft.com/9273ff1f-382e-4c58-b571-4852545915b3">MFTIME</a>



<a href="https://msdn.microsoft.com/cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5">Presentation Clock</a>
 

 

