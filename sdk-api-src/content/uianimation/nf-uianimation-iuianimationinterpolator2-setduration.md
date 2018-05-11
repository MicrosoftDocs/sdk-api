---
UID: NF:uianimation.IUIAnimationInterpolator2.SetDuration
title: IUIAnimationInterpolator2::SetDuration
author: windows-driver-content
description: Sets the duration of the transition in the given dimension.
old-location: uianimation\iuianimationinterpolator2_setduration.htm
old-project: UIAnimation
ms.assetid: C1E6EC87-283A-4C56-96C5-531C5C5F5575
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IUIAnimationInterpolator2 interface [Windows Animation],SetDuration method, IUIAnimationInterpolator2.SetDuration, IUIAnimationInterpolator2::SetDuration, SetDuration, SetDuration method [Windows Animation], SetDuration method [Windows Animation],IUIAnimationInterpolator2 interface, uianimation.iuianimationinterpolator2_setduration, uianimation/IUIAnimationInterpolator2::SetDuration
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAnimation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationInterpolator2.SetDuration
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationInterpolator2::SetDuration


## -description


Sets the duration of the transition in the given dimension.


## -parameters




### -param duration [in, out]

The duration of the transition.


## -returns



Returns <b>S_OK</b> if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Windows Animation calls this method only after calling the <a href="https://msdn.microsoft.com/DC6F046E-1A35-4FB9-9016-853AF2B598DE">IUIAnimationInterpolator2::GetDependencies</a> method, and only if that call returns <b>UI_ANIMATION_DEPENDENCY_DURATION</b> as one of its <i>durationDependencies</i> flags.

Typically, an interpolator with a duration dependency has a duration parameter in the <a href="https://msdn.microsoft.com/62aec8da-e067-4b61-9465-e07fb5b42b7f">IUIAnimationTransitionFactory</a> or <a href="https://msdn.microsoft.com/EB829B6A-770C-486A-9BA2-4D7C8F073C8F">IUIAnimationTransitionFactory2</a> creation method  that is associated with that interpolator.  The interpolator should store its duration when first initialized and overwrite the duration when <b>SetDuration</b> is called.

Windows Animation always calls the <a href="https://msdn.microsoft.com/F1C0C54D-86C3-4B65-96A4-66D89F2B2084">IUIAnimationInterpolator2::SetInitialValueAndVelocity</a> method to set the initial value and velocity before calling <b>SetDuration</b>, so a custom interpolator doesn't need to check whether the initial value and velocity have been set.

Windows Animation can call <a href="https://msdn.microsoft.com/F1C0C54D-86C3-4B65-96A4-66D89F2B2084">SetInitialValueAndVelocity</a> and <b>SetDuration</b> multiple times with different parameters. Interpolators can cache internal state to improve performance, but they must update this cached state each time <b>SetInitialValueAndVelocity</b> is called and ensure that the results of subsequent calls to <b>SetDuration</b> reflect the updated state.




## -see-also




<a href="https://msdn.microsoft.com/EC0D1933-37C3-41E2-AB13-DA4AAF4B8F04">IUIAnimationInterpolator2</a>



<a href="https://msdn.microsoft.com/3620723e-5c9b-4d6a-8576-9017fa449a5d">UI_ANIMATION_DEPENDENCIES</a>



<a href="https://msdn.microsoft.com/0745b227-61c4-462e-8529-9402c9eaa70a">UI_ANIMATION_SECONDS</a>
 

 

