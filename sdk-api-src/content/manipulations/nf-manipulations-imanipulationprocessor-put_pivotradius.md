---
UID: NF:manipulations.IManipulationProcessor.put_PivotRadius
title: IManipulationProcessor::put_PivotRadius (manipulations.h)
description: The PivotRadius property is used to determine how much rotation is used in single finger manipulation. (Put)
helpviewer_keywords: ["IManipulationProcessor interface [Windows Touch]","PivotRadius property","IManipulationProcessor.PivotRadius","IManipulationProcessor.put_PivotRadius","IManipulationProcessor::PivotRadius","IManipulationProcessor::get_PivotRadius","IManipulationProcessor::put_PivotRadius","PivotRadius property [Windows Touch]","PivotRadius property [Windows Touch]","IManipulationProcessor interface","manipulations/IManipulationProcessor::PivotRadius","manipulations/IManipulationProcessor::get_PivotRadius","manipulations/IManipulationProcessor::put_PivotRadius","put_PivotRadius","wintouch.imanipulationprocessor_pivotradius"]
old-location: wintouch\imanipulationprocessor_pivotradius.htm
tech.root: wintouch
ms.assetid: 793999b6-abb1-4912-9e9c-764f6f68ea29
ms.date: 12/05/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],PivotRadius property, IManipulationProcessor.PivotRadius, IManipulationProcessor.put_PivotRadius, IManipulationProcessor::PivotRadius, IManipulationProcessor::get_PivotRadius, IManipulationProcessor::put_PivotRadius, PivotRadius property [Windows Touch], PivotRadius property [Windows Touch],IManipulationProcessor interface, manipulations/IManipulationProcessor::PivotRadius, manipulations/IManipulationProcessor::get_PivotRadius, manipulations/IManipulationProcessor::put_PivotRadius, put_PivotRadius, wintouch.imanipulationprocessor_pivotradius
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
 - IManipulationProcessor::put_PivotRadius
 - manipulations/IManipulationProcessor::put_PivotRadius
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
 - IManipulationProcessor.PivotRadius
 - IManipulationProcessor.get_PivotRadius
 - IManipulationProcessor.put_PivotRadius
---

# IManipulationProcessor::put_PivotRadius


## -description

The <b>PivotRadius</b> property is used to determine how much rotation is used in single finger manipulation.

This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  The pivot radius must either be negative, 0, or a value greater than 1. Setting the pivot radius to a value between 0.0 and 1.0 will return <b>E_INVALIDARG</b>.
      </div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx">PivotPointX</a>



<a href="/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy">PivotPointY</a>



<a href="/windows/desktop/wintouch/mtproperties">Properties</a>



<a href="/windows/desktop/wintouch/single-finger-rotation">Single Finger Rotation</a>
