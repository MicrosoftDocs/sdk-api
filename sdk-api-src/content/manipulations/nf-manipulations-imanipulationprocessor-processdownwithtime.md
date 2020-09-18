---
UID: NF:manipulations.IManipulationProcessor.ProcessDownWithTime
title: IManipulationProcessor::ProcessDownWithTime (manipulations.h)
description: Feeds touch down data, including a timestamp, to the manipulation processor associated with a target.
helpviewer_keywords: ["IManipulationProcessor interface [Windows Touch]","ProcessDownWithTime method","IManipulationProcessor.ProcessDownWithTime","IManipulationProcessor::ProcessDownWithTime","ProcessDownWithTime","ProcessDownWithTime method [Windows Touch]","ProcessDownWithTime method [Windows Touch]","IManipulationProcessor interface","manipulations/IManipulationProcessor::ProcessDownWithTime","wintouch.imanpiulationprocessor_processdownwithtime"]
old-location: wintouch\imanpiulationprocessor_processdownwithtime.htm
tech.root: wintouch
ms.assetid: a76c9150-49b8-4a74-8ef0-bfa5ce9ec28a
ms.date: 12/05/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],ProcessDownWithTime method, IManipulationProcessor.ProcessDownWithTime, IManipulationProcessor::ProcessDownWithTime, ProcessDownWithTime, ProcessDownWithTime method [Windows Touch], ProcessDownWithTime method [Windows Touch],IManipulationProcessor interface, manipulations/IManipulationProcessor::ProcessDownWithTime, wintouch.imanpiulationprocessor_processdownwithtime
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IManipulationProcessor::ProcessDownWithTime
 - manipulations/IManipulationProcessor::ProcessDownWithTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - manipulations.h
api_name:
 - IManipulationProcessor.ProcessDownWithTime
---

# IManipulationProcessor::ProcessDownWithTime


## -description

Feeds touch down data, including a timestamp, to the manipulation processor associated with a target.

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
    you should extract the timestamp from the <a href="/windows/desktop/api/winuser/ns-winuser-touchinput">TOUCHINPUT</a> structure when you process events.


#### Examples


```cpp
static void ProcessDown(TOUCHINPUT* pTouchInput, IManipulationProcessor* pManipulationProcessor){
  pManipulationProcessor->ProcessDownWithTime(
    pTouchInput->dwID, 
    static_cast<float>(pTouchInput->x), 
    static_cast<float>(pTouchInput->y), 
    pTouchInput->dwTime
  );
}
    
```

## -see-also

<a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a>



<a href="/windows/desktop/wintouch/mtmethods">Methods</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdown">ProcessDown</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime">ProcessMoveWithTime</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processupwithtime">ProcessUpWithTime</a>