---
UID: NF:winuser.PackTouchHitTestingProximityEvaluation
title: PackTouchHitTestingProximityEvaluation function (winuser.h)
description: Returns the proximity evaluation score and the adjusted touch-point coordinates as a packed value for the WM_TOUCHHITTESTING callback.
helpviewer_keywords: ["PackTouchHitTestingProximityEvaluation","PackTouchHitTestingProximityEvaluation function","input_touchhittest.packtouchhittestingproximityevaluation","touch_hittest.packtouchhittestingproximityevaluation","winuser/PackTouchHitTestingProximityEvaluation"]
old-location: input_touchhittest\packtouchhittestingproximityevaluation.htm
tech.root: controls
ms.assetid: c4061285-2d0f-4404-9b63-bda2ec61b764
ms.date: 12/05/2018
ms.keywords: PackTouchHitTestingProximityEvaluation, PackTouchHitTestingProximityEvaluation function, input_touchhittest.packtouchhittestingproximityevaluation, touch_hittest.packtouchhittestingproximityevaluation, winuser/PackTouchHitTestingProximityEvaluation
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
 - PackTouchHitTestingProximityEvaluation
 - winuser/PackTouchHitTestingProximityEvaluation
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
 - PackTouchHitTestingProximityEvaluation
---

# PackTouchHitTestingProximityEvaluation function


## -description

Returns the proximity evaluation score and the adjusted touch-point coordinates as a packed value for the <a href="/windows/win32/inputmsg/wm-touchhittesting">WM_TOUCHHITTESTING</a> callback.

## -parameters

### -param pHitTestingInput [in]

The <a href="/windows/desktop/api/winuser/ns-winuser-touch_hit_testing_input">TOUCH_HIT_TESTING_INPUT</a> structure that holds the data for the touch contact area.

### -param pProximityEval [in]

The <a href="/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation">TOUCH_HIT_TESTING_PROXIMITY_EVALUATION</a> structure that holds the score and adjusted touch-point data that the <a href="/windows/desktop/api/winuser/nf-winuser-evaluateproximitytopolygon">EvaluateProximityToPolygon</a> or <a href="/windows/desktop/api/winuser/nf-winuser-evaluateproximitytorect">EvaluateProximityToRect</a> function returns.

## -returns

If this function succeeds, it returns the <b>score</b> and <b>adjustedPoint</b> values from <a href="/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation">TOUCH_HIT_TESTING_PROXIMITY_EVALUATION</a> as an LRESULT. To retrieve extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

## -remarks

Usually, this is the last function that's called in a <a href="/windows/win32/inputmsg/wm-touchhittesting">WM_TOUCHHITTESTING</a>  handler.

## -see-also

<a href="/previous-versions/windows/desktop/input_touchhittest/functions">Functions</a>



<a href="/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores">Touch Hit Testing Scores</a>