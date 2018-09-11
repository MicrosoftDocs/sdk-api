---
UID: NS:winuser.tagTOUCH_HIT_TESTING_PROXIMITY_EVALUATION
title: tagTOUCH_HIT_TESTING_PROXIMITY_EVALUATION
author: windows-sdk-content
description: Contains the hit test score that indicates whether the object is the likely target of the touch contact area, relative to other objects that intersect the touch contact area.
old-location: input_touchhittest\touch_hit_testing_proximity_evaluation.htm
tech.root: Input_TouchHitTest
ms.assetid: a26facc3-fe63-4657-9bd6-821dd89cb11d
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PTOUCH_HIT_TESTING_PROXIMITY_EVALUATION, PTOUCH_HIT_TESTING_PROXIMITY_EVALUATION, PTOUCH_HIT_TESTING_PROXIMITY_EVALUATION structure pointer, TOUCH_HIT_TESTING_PROXIMITY_EVALUATION, TOUCH_HIT_TESTING_PROXIMITY_EVALUATION structure, input_touchhittest.touch_hit_testing_proximity_evaluation, tagTOUCH_HIT_TESTING_PROXIMITY_EVALUATION, touch_hittest.touch_hit_testing_proximity_evaluation, winuser/PTOUCH_HIT_TESTING_PROXIMITY_EVALUATION, winuser/TOUCH_HIT_TESTING_PROXIMITY_EVALUATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
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
 - HeaderDef
api_location:
 - winuser.h
api_name:
 - TOUCH_HIT_TESTING_PROXIMITY_EVALUATION
product: Windows
targetos: Windows
req.typenames: TOUCH_HIT_TESTING_PROXIMITY_EVALUATION, *PTOUCH_HIT_TESTING_PROXIMITY_EVALUATION
req.redist: 
---

# tagTOUCH_HIT_TESTING_PROXIMITY_EVALUATION structure


## -description


Contains the hit test score that indicates whether  the object is the  likely target of the touch contact area, relative to other objects that intersect the touch contact area.


## -struct-fields




### -field score

The score, compared to the other objects that intersect the touch contact area. 


### -field adjustedPoint

The adjusted touch point that hits the closest object that's identified by the value of <i>Score</i>.



## -remarks



The <a href="https://msdn.microsoft.com/269ef4c1-9c9f-4bd7-9852-e82c4a707d3c">EvaluateProximityToRect</a> or <a href="https://msdn.microsoft.com/443d12f2-9f26-4e1e-9bf3-cd97b4026399">EvaluateProximityToPolygon</a> function returns the values.




## -see-also




<a href="https://msdn.microsoft.com/75528CC6-0637-4CAB-9187-AEC4291C119D">Structures</a>
 

 

