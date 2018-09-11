---
UID: NF:uianimation.IUIAnimationInterpolator.InterpolateValue
title: IUIAnimationInterpolator::InterpolateValue
author: windows-sdk-content
description: Interpolates the value of an animation variable at the specified offset.
old-location: uianimation\iuianimationinterpolator_interpolatevalue.htm
tech.root: UIAnimation
ms.assetid: 5f1cccd7-8b22-47a3-9704-0f22a1431c99
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUIAnimationInterpolator interface [Windows Animation],InterpolateValue method, IUIAnimationInterpolator.InterpolateValue, IUIAnimationInterpolator::InterpolateValue, InterpolateValue, InterpolateValue method [Windows Animation], InterpolateValue method [Windows Animation],IUIAnimationInterpolator interface, uianimation.iuianimationinterpolator_interpolatevalue, uianimation/IUIAnimationInterpolator::InterpolateValue
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationInterpolator.InterpolateValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationInterpolator::InterpolateValue


## -description


Interpolates the value of an animation variable at the specified offset.


## -parameters




### -param offset [in]

 The offset from the start of the transition.

This parameter is always greater than or equal to zero and less than the duration of the transition. This method is not called if the duration of the transition is zero.


### -param value [out]

The interpolated value.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Windows Animation always calls the <a href="https://msdn.microsoft.com/a1c5451a-b8d0-4eb7-883c-6bd1d585cb11">SetInitialValueAndVelocity</a> method to set the initial value and velocity before calling <b>InterpolateValue</b>, so a custom interpolator need not check whether the initial value and velocity have been set.

Windows Animation can call <a href="https://msdn.microsoft.com/a1c5451a-b8d0-4eb7-883c-6bd1d585cb11">SetInitialValueAndVelocity</a> multiple times with different parameters. Interpolators can cache internal state to improve performance, but they must update this cached state each time <b>SetInitialValueAndVelocity</b> is called and ensure that the results of subsequent calls to <b>InterpolateValue</b> reflect the updated state.




## -see-also




<a href="https://msdn.microsoft.com/8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc">IUIAnimationInterpolator</a>



<a href="https://msdn.microsoft.com/0745b227-61c4-462e-8529-9402c9eaa70a">UI_ANIMATION_SECONDS</a>
 

 

