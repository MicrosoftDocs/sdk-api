---
UID: NF:uianimation.IUIAnimationInterpolator.InterpolateVelocity
title: IUIAnimationInterpolator::InterpolateVelocity
author: windows-sdk-content
description: Interpolates the velocity, or rate of change, at the specified offset.
old-location: uianimation\iuianimationinterpolator_interpolatevelocity.htm
old-project: UIAnimation
ms.assetid: ae0b6674-307b-454e-b8be-db564c234607
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IUIAnimationInterpolator interface [Windows Animation],InterpolateVelocity method, IUIAnimationInterpolator.InterpolateVelocity, IUIAnimationInterpolator::InterpolateVelocity, InterpolateVelocity, InterpolateVelocity method [Windows Animation], InterpolateVelocity method [Windows Animation],IUIAnimationInterpolator interface, uianimation.iuianimationinterpolator_interpolatevelocity, uianimation/IUIAnimationInterpolator::InterpolateVelocity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps \| UWP apps]
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
tech.root: 
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationInterpolator.InterpolateVelocity
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationInterpolator::InterpolateVelocity


## -description


Interpolates the velocity, or rate of change, at the specified offset.


## -parameters




### -param offset [in]

The offset from the start of the transition.

The offset is always greater than or equal to zero and less than or equal to the duration of the transition. This method is not called if the duration of the transition is zero.


### -param velocity [out]

The interpolated velocity.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Windows Animation always calls the <a href="https://msdn.microsoft.com/a1c5451a-b8d0-4eb7-883c-6bd1d585cb11">SetInitialValueAndVelocity</a> method to set the initial value and velocity before calling <b>InterpolateVelocity</b>, so a custom interpolator need not check whether the initial value and velocity have been set.

Windows Animation can call <a href="https://msdn.microsoft.com/a1c5451a-b8d0-4eb7-883c-6bd1d585cb11">SetInitialValueAndVelocity</a> multiple times with different parameters. Interpolators can cache internal state to improve performance, but they must update this cached state each time <b>SetInitialValueAndVelocity</b> is called and ensure that the results of subsequent calls to <b>InterpolateVelocity</b> reflect the updated state.




## -see-also




<a href="https://msdn.microsoft.com/8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc">IUIAnimationInterpolator</a>



<a href="https://msdn.microsoft.com/0745b227-61c4-462e-8529-9402c9eaa70a">UI_ANIMATION_SECONDS</a>
 

 

