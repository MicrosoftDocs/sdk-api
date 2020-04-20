---
UID: NF:manipulations.IManipulationProcessor.get_PivotRadius
title: IManipulationProcessor::get_PivotRadius (manipulations.h)
description: The PivotRadius property is used to determine how much rotation is used in single finger manipulation.helpviewer_keywords: ["IManipulationProcessor interface [Windows Touch]","PivotRadius property","IManipulationProcessor.PivotRadius","IManipulationProcessor.get_PivotRadius","IManipulationProcessor::PivotRadius","IManipulationProcessor::get_PivotRadius","IManipulationProcessor::put_PivotRadius","PivotRadius property [Windows Touch]","PivotRadius property [Windows Touch]","IManipulationProcessor interface","get_PivotRadius","manipulations/IManipulationProcessor::PivotRadius","manipulations/IManipulationProcessor::get_PivotRadius","manipulations/IManipulationProcessor::put_PivotRadius","wintouch.imanipulationprocessor_pivotradius"]
old-location: wintouch\imanipulationprocessor_pivotradius.htm
tech.root: wintouch
ms.assetid: 793999b6-abb1-4912-9e9c-764f6f68ea29
ms.date: 12/05/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],PivotRadius property, IManipulationProcessor.PivotRadius, IManipulationProcessor.get_PivotRadius, IManipulationProcessor::PivotRadius, IManipulationProcessor::get_PivotRadius, IManipulationProcessor::put_PivotRadius, PivotRadius property [Windows Touch], PivotRadius property [Windows Touch],IManipulationProcessor interface, get_PivotRadius, manipulations/IManipulationProcessor::PivotRadius, manipulations/IManipulationProcessor::get_PivotRadius, manipulations/IManipulationProcessor::put_PivotRadius, wintouch.imanipulationprocessor_pivotradius
f1_keywords:
- manipulations/IManipulationProcessor.PivotRadius
dev_langs:
- c++
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
- IManipulationProcessor.PivotRadius
- IManipulationProcessor.get_PivotRadius
- IManipulationProcessor.put_PivotRadius
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IManipulationProcessor::get_PivotRadius


## -description


The <b>PivotRadius</b> property is used to determine how much rotation is used in single finger manipulation.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  The pivot radius must either be negative, 0, or a value greater than 1. Setting the pivot radius to a value between 0.0 and 1.0 will return <b>E_INVALIDARG</b>.
      </div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor">IManipulationProcessor</a>



<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointx">PivotPointX</a>



<a href="https://docs.microsoft.com/windows/desktop/api/manipulations/nf-manipulations-imanipulationprocessor-get_pivotpointy">PivotPointY</a>



<a href="https://docs.microsoft.com/windows/desktop/wintouch/mtproperties">Properties</a>



<a href="https://docs.microsoft.com/windows/desktop/wintouch/single-finger-rotation">Single Finger Rotation</a>
 

 

