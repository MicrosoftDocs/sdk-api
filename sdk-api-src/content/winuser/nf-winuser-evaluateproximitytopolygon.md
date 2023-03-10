---
UID: NF:winuser.EvaluateProximityToPolygon
title: EvaluateProximityToPolygon function (winuser.h)
description: Returns the score of a polygon as the probable touch target (compared to all other polygons that intersect the touch contact area) and an adjusted touch point within the polygon.
helpviewer_keywords: ["EvaluateProximityToPolygon","EvaluateProximityToPolygon function","input_touchhittest.evaluateproximitytopolygon","touch_hittest.evaluateproximitytopolygon","winuser/EvaluateProximityToPolygon"]
old-location: input_touchhittest\evaluateproximitytopolygon.htm
tech.root: controls
ms.assetid: 443d12f2-9f26-4e1e-9bf3-cd97b4026399
ms.date: 12/05/2018
ms.keywords: EvaluateProximityToPolygon, EvaluateProximityToPolygon function, input_touchhittest.evaluateproximitytopolygon, touch_hittest.evaluateproximitytopolygon, winuser/EvaluateProximityToPolygon
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EvaluateProximityToPolygon
 - winuser/EvaluateProximityToPolygon
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-Touch-HitTest-l1-1-0.dll
 - MinUser.dll
api_name:
 - EvaluateProximityToPolygon
---

# EvaluateProximityToPolygon function


## -description

Returns the score of a polygon as the probable touch target (compared to all other polygons that intersect the touch contact area) and an adjusted touch point within the polygon.

## -parameters

### -param numVertices

The number of vertices in the polygon. This value must be greater than or equal to 3.

This value indicates the size of the array, as specified by the <i>controlPolygon</i> parameter.

### -param controlPolygon [in]

The array of x-y screen coordinates that define the shape of the UI element. 

The <i>numVertices</i> parameter specifies the number of coordinates.

### -param pHitTestingInput [in]

The <a href="/windows/desktop/api/winuser/ns-winuser-touch_hit_testing_input">TOUCH_HIT_TESTING_INPUT</a> structure that holds the data for the touch contact area.

### -param pProximityEval [out]

The <a href="/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation">TOUCH_HIT_TESTING_PROXIMITY_EVALUATION</a> structure that holds the score and adjusted touch-point data.

## -returns

If this function succeeds, it returns TRUE.
 
Otherwise, it returns FALSE. To retrieve extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

For consistency with Windows, frameworks that handle <a href="/windows/win32/inputmsg/wm-touchhittesting">WM_TOUCHHITTESTING</a> should use the following principles for targeting:

<ul>
<li>Inclusion: If the touch point is within the boundaries of a control, the touch point is not changed. 
</li>
<li>Intersection: Include only controls that intersect the contact geometry. 
</li>
<li>Z-order: If more than one control intersects the contact geometry, and the controls overlap, the control that's highest in the z-order receives priority. 
</li>
<li>Ambiguity: If more than one control intersects the contact geometry, and the controls don't overlap, the control that's closest to the original touch point receives priority. </li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/input_touchhittest/functions">Functions</a>