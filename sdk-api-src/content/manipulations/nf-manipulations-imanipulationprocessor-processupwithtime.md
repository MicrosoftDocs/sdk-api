---
UID: NF:manipulations.IManipulationProcessor.ProcessUpWithTime
title: IManipulationProcessor::ProcessUpWithTime (manipulations.h)
description: Feeds data, including a timestamp, to a target's manipulation processor for touch-up sequences.
helpviewer_keywords: ["IManipulationProcessor interface [Windows Touch]","ProcessUpWithTime method","IManipulationProcessor.ProcessUpWithTime","IManipulationProcessor::ProcessUpWithTime","ProcessUpWithTime","ProcessUpWithTime method [Windows Touch]","ProcessUpWithTime method [Windows Touch]","IManipulationProcessor interface","manipulations/IManipulationProcessor::ProcessUpWithTime","wintouch.imanpiulationprocessor_processupwithtime"]
old-location: wintouch\imanpiulationprocessor_processupwithtime.htm
tech.root: wintouch
ms.assetid: fafea353-9126-454d-9311-4859e5ae5712
ms.date: 12/05/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],ProcessUpWithTime method, IManipulationProcessor.ProcessUpWithTime, IManipulationProcessor::ProcessUpWithTime, ProcessUpWithTime, ProcessUpWithTime method [Windows Touch], ProcessUpWithTime method [Windows Touch],IManipulationProcessor interface, manipulations/IManipulationProcessor::ProcessUpWithTime, wintouch.imanpiulationprocessor_processupwithtime
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
 - IManipulationProcessor::ProcessUpWithTime
 - manipulations/IManipulationProcessor::ProcessUpWithTime
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
 - IManipulationProcessor.ProcessUpWithTime
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
    you should extract the timestamp from the <a href="/windows/desktop/api/winuser/ns-winuser-touchinput">TOUCHINPUT</a> structure when you process events.


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

<a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a>



<a href="/windows/desktop/wintouch/mtmethods">Methods</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime">ProcessDownWithTime</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime">ProcessMoveWithTime</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processup">ProcessUp</a>