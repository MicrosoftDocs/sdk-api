---
UID: NF:manipulations.IManipulationProcessor.ProcessDown
title: IManipulationProcessor::ProcessDown (manipulations.h)
description: The ProcessDown method feeds touch down data to the manipulation processor associated with a target.
helpviewer_keywords: ["IManipulationProcessor interface [Windows Touch]","ProcessDown method","IManipulationProcessor.ProcessDown","IManipulationProcessor::ProcessDown","ProcessDown","ProcessDown method [Windows Touch]","ProcessDown method [Windows Touch]","IManipulationProcessor interface","manipulations/IManipulationProcessor::ProcessDown","wintouch.imanipulationprocessor_processdown"]
old-location: wintouch\imanipulationprocessor_processdown.htm
tech.root: wintouch
ms.assetid: 2c192bc4-6922-4c70-961d-1f8684ad792b
ms.date: 12/05/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],ProcessDown method, IManipulationProcessor.ProcessDown, IManipulationProcessor::ProcessDown, ProcessDown, ProcessDown method [Windows Touch], ProcessDown method [Windows Touch],IManipulationProcessor interface, manipulations/IManipulationProcessor::ProcessDown, wintouch.imanipulationprocessor_processdown
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
 - IManipulationProcessor::ProcessDown
 - manipulations/IManipulationProcessor::ProcessDown
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
 - IManipulationProcessor.ProcessDown
---

# IManipulationProcessor::ProcessDown


## -description

The <b>ProcessDown</b> method feeds touch down data to the manipulation processor associated with a target.

## -parameters

### -param manipulatorId

The identifier for the touch contact that you want to process.

### -param x

The horizontal coordinate data associated with the target.

### -param y

The vertical coordinate data associated with the target.

## -returns

Returns <b>S_OK</b> on success, otherwise returns an error code such as <b>E_FAIL</b>.

## -remarks

This method takes a timestamp using system time rather than from the touch hardware. To improve the experience in 
    cases where performance is degrading you should use the <a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdownwithtime">ProcessDownWithTime</a> method.

## -see-also

<a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a>



<a href="/windows/desktop/wintouch/mtmethods">Methods</a>