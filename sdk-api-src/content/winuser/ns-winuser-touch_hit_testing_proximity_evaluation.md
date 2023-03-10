---
UID: NS:winuser.tagTOUCH_HIT_TESTING_PROXIMITY_EVALUATION
title: TOUCH_HIT_TESTING_PROXIMITY_EVALUATION (winuser.h)
description: Contains the hit test score that indicates whether the object is the likely target of the touch contact area, relative to other objects that intersect the touch contact area.
helpviewer_keywords: ["*PTOUCH_HIT_TESTING_PROXIMITY_EVALUATION","PTOUCH_HIT_TESTING_PROXIMITY_EVALUATION","PTOUCH_HIT_TESTING_PROXIMITY_EVALUATION structure pointer","TOUCH_HIT_TESTING_PROXIMITY_EVALUATION","TOUCH_HIT_TESTING_PROXIMITY_EVALUATION structure","input_touchhittest.touch_hit_testing_proximity_evaluation","tagTOUCH_HIT_TESTING_PROXIMITY_EVALUATION","touch_hittest.touch_hit_testing_proximity_evaluation","winuser/PTOUCH_HIT_TESTING_PROXIMITY_EVALUATION","winuser/TOUCH_HIT_TESTING_PROXIMITY_EVALUATION"]
old-location: input_touchhittest\touch_hit_testing_proximity_evaluation.htm
tech.root: controls
ms.assetid: a26facc3-fe63-4657-9bd6-821dd89cb11d
ms.date: 12/05/2018
ms.keywords: '*PTOUCH_HIT_TESTING_PROXIMITY_EVALUATION, PTOUCH_HIT_TESTING_PROXIMITY_EVALUATION, PTOUCH_HIT_TESTING_PROXIMITY_EVALUATION structure pointer, TOUCH_HIT_TESTING_PROXIMITY_EVALUATION, TOUCH_HIT_TESTING_PROXIMITY_EVALUATION structure, input_touchhittest.touch_hit_testing_proximity_evaluation, tagTOUCH_HIT_TESTING_PROXIMITY_EVALUATION, touch_hittest.touch_hit_testing_proximity_evaluation, winuser/PTOUCH_HIT_TESTING_PROXIMITY_EVALUATION, winuser/TOUCH_HIT_TESTING_PROXIMITY_EVALUATION'
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
req.typenames: TOUCH_HIT_TESTING_PROXIMITY_EVALUATION, *PTOUCH_HIT_TESTING_PROXIMITY_EVALUATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTOUCH_HIT_TESTING_PROXIMITY_EVALUATION
 - winuser/tagTOUCH_HIT_TESTING_PROXIMITY_EVALUATION
 - PTOUCH_HIT_TESTING_PROXIMITY_EVALUATION
 - winuser/PTOUCH_HIT_TESTING_PROXIMITY_EVALUATION
 - TOUCH_HIT_TESTING_PROXIMITY_EVALUATION
 - winuser/TOUCH_HIT_TESTING_PROXIMITY_EVALUATION
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
 - TOUCH_HIT_TESTING_PROXIMITY_EVALUATION
---

# TOUCH_HIT_TESTING_PROXIMITY_EVALUATION structure


## -description

Contains the hit test score that indicates whether  the object is the  likely target of the touch contact area, relative to other objects that intersect the touch contact area.

## -struct-fields

### -field score

The score, compared to the other objects that intersect the touch contact area.

### -field adjustedPoint

The adjusted touch point that hits the closest object that's identified by the value of <i>Score</i>.

## -remarks

The <a href="/windows/desktop/api/winuser/nf-winuser-evaluateproximitytorect">EvaluateProximityToRect</a> or <a href="/windows/desktop/api/winuser/nf-winuser-evaluateproximitytopolygon">EvaluateProximityToPolygon</a> function returns the values.

## -see-also

<a href="/previous-versions/windows/desktop/input_touchhittest/structures">Structures</a>