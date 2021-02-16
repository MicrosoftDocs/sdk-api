---
UID: NF:manipulations.IManipulationProcessor.ProcessMove
title: IManipulationProcessor::ProcessMove (manipulations.h)
description: The ProcessMove method feeds movement data for the target object to its manipulation processor.
helpviewer_keywords: ["IManipulationProcessor interface [Windows Touch]","ProcessMove method","IManipulationProcessor.ProcessMove","IManipulationProcessor::ProcessMove","ProcessMove","ProcessMove method [Windows Touch]","ProcessMove method [Windows Touch]","IManipulationProcessor interface","manipulations/IManipulationProcessor::ProcessMove","wintouch.imanipulationprocessor_processmove"]
old-location: wintouch\imanipulationprocessor_processmove.htm
tech.root: wintouch
ms.assetid: e2c0e975-3edd-43d5-8a58-2d8166413c76
ms.date: 12/05/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],ProcessMove method, IManipulationProcessor.ProcessMove, IManipulationProcessor::ProcessMove, ProcessMove, ProcessMove method [Windows Touch], ProcessMove method [Windows Touch],IManipulationProcessor interface, manipulations/IManipulationProcessor::ProcessMove, wintouch.imanipulationprocessor_processmove
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
 - IManipulationProcessor::ProcessMove
 - manipulations/IManipulationProcessor::ProcessMove
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
 - IManipulationProcessor.ProcessMove
---

# IManipulationProcessor::ProcessMove


## -description

The <b>ProcessMove</b> method feeds movement data for the target object to its manipulation processor.

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
    cases where performance is degrading you should use the <a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime">ProcessMoveWithTime</a> method.

## -see-also

<a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a>



<a href="/windows/desktop/wintouch/mtmethods">Methods</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processdown">ProcessDown</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processmovewithtime">ProcessMoveWithTime</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-processup">ProcessUp</a>