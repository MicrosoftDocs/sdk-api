---
UID: NS:winuser.tagTOUCH_HIT_TESTING_INPUT
title: tagTOUCH_HIT_TESTING_INPUT
author: windows-sdk-content
description: Contains information about the touch contact area reported by the touch digitizer.
old-location: input_touchhittest\touch_hit_testing_input.htm
old-project: Input_TouchHitTest
ms.assetid: d2103f6e-6aa9-4260-bef9-cfcbec35e675
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PTOUCH_HIT_TESTING_INPUT, PTOUCH_HIT_TESTING_INPUT, PTOUCH_HIT_TESTING_INPUT structure pointer, TOUCH_HIT_TESTING_INPUT, TOUCH_HIT_TESTING_INPUT structure, input_touchhittest.touch_hit_testing_input, tagTOUCH_HIT_TESTING_INPUT, touch_hittest.touch_hit_testing_input, winuser/PTOUCH_HIT_TESTING_INPUT, winuser/TOUCH_HIT_TESTING_INPUT"
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
tech.root: 
req.typenames: TOUCH_HIT_TESTING_INPUT, *PTOUCH_HIT_TESTING_INPUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winuser.h
api_name:
 - TOUCH_HIT_TESTING_INPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagTOUCH_HIT_TESTING_INPUT structure


## -description


Contains information about the touch contact area reported by the touch digitizer.


## -struct-fields




### -field pointerId

The ID of the pointer. You cannot pass this value to the input message process and  retrieve additional pointer info through <a href="https://msdn.microsoft.com/75faea24-91cd-448b-b67a-19fe530f1800">GetPointerInfo</a>. 


### -field point

The screen coordinates of the touch point that the touch digitizer reports.


### -field boundingBox

The bounding rectangle of the touch contact area. Valid touch targets are identified and scored based on this bounding box. 

<div class="alert"><b>Note</b>  This bounding box may differ from the contact area that the digitizer reports when:
<ul>
<li>The digitizer reports a touch contact area that's outside the maximum or minimum size threshold that's recognized by  <a href="https://msdn.microsoft.com/bdd7630c-b2d8-4080-a149-efec018f697d">Touch Hit Testing</a>.</li>
<li>A portion of the touch contact area is occluded by another object that's higher in the z-order.
</li>
</ul>
</div>
<div> </div>

### -field nonOccludedBoundingBox

The touch contact area within a specific targeted window that's not occluded by other objects that are higher in the z-order. Any area that's occluded by another object is an invalid target.


### -field orientation

The orientation of the touch contact area.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

