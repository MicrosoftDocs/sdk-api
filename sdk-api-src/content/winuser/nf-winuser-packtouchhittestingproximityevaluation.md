---
UID: NF:winuser.PackTouchHitTestingProximityEvaluation
title: PackTouchHitTestingProximityEvaluation function
author: windows-sdk-content
description: Returns the proximity evaluation score and the adjusted touch-point coordinates as a packed value for the WM_TOUCHHITTESTING callback.
old-location: input_touchhittest\packtouchhittestingproximityevaluation.htm
old-project: Input_TouchHitTest
ms.assetid: c4061285-2d0f-4404-9b63-bda2ec61b764
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: PackTouchHitTestingProximityEvaluation, PackTouchHitTestingProximityEvaluation function, input_touchhittest.packtouchhittestingproximityevaluation, touch_hittest.packtouchhittestingproximityevaluation, winuser/PackTouchHitTestingProximityEvaluation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: 
req.redist: 
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
req.typenames: 
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
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# PackTouchHitTestingProximityEvaluation function


## -description


Returns the proximity evaluation score and the adjusted touch-point coordinates as a packed value for the <a href="https://msdn.microsoft.com/741F9D67-A914-46CF-91A3-EF40447E7438">WM_TOUCHHITTESTING</a> callback.  




## -parameters




### -param pHitTestingInput [in]

The <a href="https://msdn.microsoft.com/d2103f6e-6aa9-4260-bef9-cfcbec35e675">TOUCH_HIT_TESTING_INPUT</a> structure that holds the data for the touch contact area. 


### -param pProximityEval [in]

The <a href="https://msdn.microsoft.com/a26facc3-fe63-4657-9bd6-821dd89cb11d">TOUCH_HIT_TESTING_PROXIMITY_EVALUATION</a> structure that holds the score and adjusted touch-point data that the <a href="https://msdn.microsoft.com/443d12f2-9f26-4e1e-9bf3-cd97b4026399">EvaluateProximityToPolygon</a> or <a href="https://msdn.microsoft.com/269ef4c1-9c9f-4bd7-9852-e82c4a707d3c">EvaluateProximityToRect</a> function returns.


## -returns



If this function succeeds, it returns the <b>score</b> and <b>adjustedPoint</b> values from <a href="https://msdn.microsoft.com/a26facc3-fe63-4657-9bd6-821dd89cb11d">TOUCH_HIT_TESTING_PROXIMITY_EVALUATION</a> as an LRESULT. To retrieve extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.
 




## -remarks



Usually, this is the last function that's called in a <a href="https://msdn.microsoft.com/741F9D67-A914-46CF-91A3-EF40447E7438">WM_TOUCHHITTESTING</a>  handler.




## -see-also




<a href="https://msdn.microsoft.com/C7275A12-4F76-485D-896F-3CCB8CE92F8E">Functions</a>



<a href="https://msdn.microsoft.com/EACDE6DB-ADBD-4F0C-8C31-7321AB6A73EA">Touch Hit Testing Scores</a>
 

 

