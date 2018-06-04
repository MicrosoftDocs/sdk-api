---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IManipulationProcessor::get_PivotRadius


## -description


The <b>PivotRadius</b> property is used to determine how much rotation is used in single finger manipulation.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  
The pivot radius must either be negative, 0, or a value greater than 1. Setting the pivot radius to a value between 0.0 and 1.0 will return <b>E_INVALIDARG</b>.
      </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/963f87c1-e128-4bd5-9f28-d49418f768fb">IManipulationProcessor</a>



<a href="https://msdn.microsoft.com/52afdf21-8c5d-4da8-aab2-7a8273df5147">PivotPointX</a>



<a href="https://msdn.microsoft.com/09faaacd-3583-4129-b8e3-068e34e220b7">PivotPointY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff542598">Properties</a>



<a href="https://msdn.microsoft.com/b9c19009-8ac0-4168-bf26-393280fc589f">Single Finger Rotation</a>
 

 

