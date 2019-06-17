---
UID: NF:manipulations.IManipulationProcessor.ProcessMoveWithTime
title: IManipulationProcessor::ProcessMoveWithTime (manipulations.h)
author: windows-sdk-content
description: Feeds movement data, including a time stamp, for the target object to its manipulation processor.
old-location: wintouch\imanpiulationprocessor_processmovewithtime.htm
tech.root: wintouch
ms.assetid: 0840ef85-9b18-4248-96fe-93653274a89a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],ProcessMoveWithTime method, IManipulationProcessor.ProcessMoveWithTime, IManipulationProcessor::ProcessMoveWithTime, ProcessMoveWithTime, ProcessMoveWithTime method [Windows Touch], ProcessMoveWithTime method [Windows Touch],IManipulationProcessor interface, manipulations/IManipulationProcessor::ProcessMoveWithTime, wintouch.imanpiulationprocessor_processmovewithtime
ms.topic: method
f1_keywords: ["manipulations/IManipulationProcessor.ProcessMoveWithTime"]
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
 - IManipulationProcessor.ProcessMoveWithTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IManipulationProcessor::ProcessMoveWithTime


## -description


Feeds movement data, including a time stamp, for the target object to its manipulation processor.


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
    you should extract the time stamp from the <a href="https://docs.microsoft.com/windows/desktop/api/winuser/ns-winuser-tagtouchinput">TOUCHINPUT</a> structure when you process events.


#### Examples


```cpp

static void ProcessMove(TOUCHINPUT* pTouchInput, IManipulationProcessor* pManipulationProcessor){
  pManipulationProcessor->ProcessMoveWithTime(
    pTouchInput->dwID, 
    static_cast<float>(pTouchInput->x), 
    static_cast<float>(pTouchInput->y), 
    pTouchInput->dwTime
  );
}
      
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a>



<a href="https://docs.microsoft.com/windows/desktop/wintouch/mtmethods">Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime">ProcessDownWithTime</a>



<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmove">ProcessMove</a>



<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime">ProcessUpWithTime</a>
 

 

