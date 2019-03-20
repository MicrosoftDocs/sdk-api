---
UID: NF:manipulations.IManipulationProcessor.ProcessUpWithTime
title: IManipulationProcessor::ProcessUpWithTime (manipulations.h)
author: windows-sdk-content
description: Feeds data, including a timestamp, to a target's manipulation processor for touch-up sequences.
old-location: wintouch\imanpiulationprocessor_processupwithtime.htm
tech.root: wintouch
ms.assetid: fafea353-9126-454d-9311-4859e5ae5712
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],ProcessUpWithTime method, IManipulationProcessor.ProcessUpWithTime, IManipulationProcessor::ProcessUpWithTime, ProcessUpWithTime, ProcessUpWithTime method [Windows Touch], ProcessUpWithTime method [Windows Touch],IManipulationProcessor interface, manipulations/IManipulationProcessor::ProcessUpWithTime, wintouch.imanpiulationprocessor_processupwithtime
ms.topic: method
req.header: manipulations.h
req.include-header: Manipulations_i.c
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - manipulations.h
api_name:
 - IManipulationProcessor.ProcessUpWithTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IManipulationProcessor::ProcessUpWithTime


## -description


Feeds data, including a timestamp, to a target's manipulation processor for touch-up sequences.


## -parameters




### -param manipulatorId

The identifier for the touch contact to be processed.


### -param x

The horizontal coordinate data associated with the target.


### -param y

The vertical coordinate data associated with the target.


### -param timestamp

The time of the data event.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an HRESULT error code such as <b>E_FAIL</b>.




## -remarks



It is possible to receive touch events out of the order they were produced.  To fix this, 
    you should extract the timestamp from the <a href="https://msdn.microsoft.com/fc382759-3a1e-401e-a6a7-1bf209a5434b">TOUCHINPUT</a> structure when you process events.


#### Examples


```cpp

static void ProcessUp(TOUCHINPUT* pTouchInput, IManipulationProcessor* pManipulationProcessor){
  pManipulationProcessor->ProcessUpWithTime(
    pTouchInput->dwID, 
    static_cast<float>(pTouchInput->x), 
    static_cast<float>(pTouchInput->y), 
    pTouchInput->dwTime
  );
}
```





## -see-also




<a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a>



<a href="https://msdn.microsoft.com/33736f79-cb61-449c-80b9-1358db2621e9">Methods</a>



<a href="https://msdn.microsoft.com/a76c9150-49b8-4a74-8ef0-bfa5ce9ec28a">ProcessDownWithTime</a>



<a href="https://msdn.microsoft.com/0840ef85-9b18-4248-96fe-93653274a89a">ProcessMoveWithTime</a>



<a href="https://msdn.microsoft.com/c93f6729-5e50-41a1-867c-93e4ce9ecda9">ProcessUp</a>
 

 

