---
UID: NF:manipulations.IManipulationProcessor.put_PivotRadius
title: IManipulationProcessor::put_PivotRadius
author: windows-sdk-content
description: The PivotRadius property is used to determine how much rotation is used in single finger manipulation.
old-location: wintouch\imanipulationprocessor_pivotradius.htm
old-project: wintouch
ms.assetid: 793999b6-abb1-4912-9e9c-764f6f68ea29
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IManipulationProcessor interface [Windows Touch],PivotRadius property, IManipulationProcessor.PivotRadius, IManipulationProcessor.put_PivotRadius, IManipulationProcessor::PivotRadius, IManipulationProcessor::get_PivotRadius, IManipulationProcessor::put_PivotRadius, PivotRadius property [Windows Touch], PivotRadius property [Windows Touch],IManipulationProcessor interface, manipulations/IManipulationProcessor::PivotRadius, manipulations/IManipulationProcessor::get_PivotRadius, manipulations/IManipulationProcessor::put_PivotRadius, put_PivotRadius, wintouch.imanipulationprocessor_pivotradius
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: manipulations.h
req.include-header: Manipulations_i.c
req.redist: 
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
tech.root: 
req.typenames: MANIPULATION_PROCESSOR_MANIPULATIONS
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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




<a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a>



<a href="https://msdn.microsoft.com/52afdf21-8c5d-4da8-aab2-7a8273df5147">PivotPointX</a>



<a href="https://msdn.microsoft.com/09faaacd-3583-4129-b8e3-068e34e220b7">PivotPointY</a>



<a href="https://msdn.microsoft.com/0f8a3e27-a92f-4086-9573-6c7bbe7efd20">Properties</a>



<a href="https://msdn.microsoft.com/b9c19009-8ac0-4168-bf26-393280fc589f">Single Finger Rotation</a>
 

 

