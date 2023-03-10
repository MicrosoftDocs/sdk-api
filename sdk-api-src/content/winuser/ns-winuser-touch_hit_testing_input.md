---
UID: NS:winuser.tagTOUCH_HIT_TESTING_INPUT
title: TOUCH_HIT_TESTING_INPUT (winuser.h)
description: Contains information about the touch contact area reported by the touch digitizer.
helpviewer_keywords: ["*PTOUCH_HIT_TESTING_INPUT","PTOUCH_HIT_TESTING_INPUT","PTOUCH_HIT_TESTING_INPUT structure pointer","TOUCH_HIT_TESTING_INPUT","TOUCH_HIT_TESTING_INPUT structure","input_touchhittest.touch_hit_testing_input","tagTOUCH_HIT_TESTING_INPUT","touch_hittest.touch_hit_testing_input","winuser/PTOUCH_HIT_TESTING_INPUT","winuser/TOUCH_HIT_TESTING_INPUT"]
old-location: input_touchhittest\touch_hit_testing_input.htm
tech.root: controls
ms.assetid: d2103f6e-6aa9-4260-bef9-cfcbec35e675
ms.date: 12/05/2018
ms.keywords: '*PTOUCH_HIT_TESTING_INPUT, PTOUCH_HIT_TESTING_INPUT, PTOUCH_HIT_TESTING_INPUT structure pointer, TOUCH_HIT_TESTING_INPUT, TOUCH_HIT_TESTING_INPUT structure, input_touchhittest.touch_hit_testing_input, tagTOUCH_HIT_TESTING_INPUT, touch_hittest.touch_hit_testing_input, winuser/PTOUCH_HIT_TESTING_INPUT, winuser/TOUCH_HIT_TESTING_INPUT'
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
targetos: Windows
req.typenames: TOUCH_HIT_TESTING_INPUT, *PTOUCH_HIT_TESTING_INPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTOUCH_HIT_TESTING_INPUT
 - winuser/tagTOUCH_HIT_TESTING_INPUT
 - PTOUCH_HIT_TESTING_INPUT
 - winuser/PTOUCH_HIT_TESTING_INPUT
 - TOUCH_HIT_TESTING_INPUT
 - winuser/TOUCH_HIT_TESTING_INPUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winuser.h
api_name:
 - TOUCH_HIT_TESTING_INPUT
---

# TOUCH_HIT_TESTING_INPUT structure


## -description

Contains information about the touch contact area reported by the touch digitizer.

## -struct-fields

### -field pointerId

The ID of the pointer. You cannot pass this value to the input message process and  retrieve additional pointer info through <a href="/windows/desktop/api/winuser/nf-winuser-getpointerinfo">GetPointerInfo</a>.

### -field point

The screen coordinates of the touch point that the touch digitizer reports.

### -field boundingBox

The bounding rectangle of the touch contact area. Valid touch targets are identified and scored based on this bounding box. 

<div class="alert"><b>Note</b>  This bounding box may differ from the contact area that the digitizer reports when:
<ul>
<li>The digitizer reports a touch contact area that's outside the maximum or minimum size threshold that's recognized by  <a href="/previous-versions/windows/desktop/input_touchhittest/touch-hit-testing-portal">Touch Hit Testing</a>.</li>
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

<a href="/previous-versions/windows/desktop/input_touchhittest/structures">Structures</a>