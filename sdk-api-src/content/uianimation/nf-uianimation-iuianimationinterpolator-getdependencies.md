---
UID: NF:uianimation.IUIAnimationInterpolator.GetDependencies
title: IUIAnimationInterpolator::GetDependencies
author: windows-sdk-content
description: Gets the aspects of the interpolator that depend on the initial value or velocity passed to SetInitialValueAndVelocity, or that depend on the duration passed to SetDuration.
old-location: uianimation\iuianimationinterpolator_getdependencies.htm
old-project: UIAnimation
ms.assetid: a897caa9-8a03-465e-8b74-b4614efce00c
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetDependencies, GetDependencies method [Windows Animation], GetDependencies method [Windows Animation],IUIAnimationInterpolator interface, IUIAnimationInterpolator interface [Windows Animation],GetDependencies method, IUIAnimationInterpolator.GetDependencies, IUIAnimationInterpolator::GetDependencies, uianimation.iuianimationinterpolator_getdependencies, uianimation/IUIAnimationInterpolator::GetDependencies
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps | UWP apps]
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
-	IUIAnimationInterpolator.GetDependencies
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationInterpolator::GetDependencies


## -description



   
   Gets the aspects of the interpolator that depend on the initial value or velocity passed to <a href="https://msdn.microsoft.com/a1c5451a-b8d0-4eb7-883c-6bd1d585cb11">SetInitialValueAndVelocity</a>, or that depend on the duration passed to <a href="https://msdn.microsoft.com/79038ada-ebc2-4259-862a-d81403c2f6b8">SetDuration</a>.


## -parameters




### -param initialValueDependencies [out]


                
                Aspects of the interpolator that depend on the  initial value passed to <a href="https://msdn.microsoft.com/a1c5451a-b8d0-4eb7-883c-6bd1d585cb11">SetInitialValueAndVelocity</a>.


### -param initialVelocityDependencies [out]


                
                Aspects of the interpolator that depend on the initial velocity passed to <a href="https://msdn.microsoft.com/a1c5451a-b8d0-4eb7-883c-6bd1d585cb11">SetInitialValueAndVelocity</a>.


### -param durationDependencies [out]

Aspects of the interpolator that depend on the duration passed to <a href="https://msdn.microsoft.com/79038ada-ebc2-4259-862a-d81403c2f6b8">SetDuration</a>.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method is called to identify which aspects of the custom interpolator are affected by certain inputs: value, velocity, and duration. For each of these inputs, the interpolator returns either of the following:

<ul>
<li>The bitwise-OR of any members of <a href="https://msdn.microsoft.com/3620723e-5c9b-4d6a-8576-9017fa449a5d">UI_ANIMATION_DEPENDENCIES</a> that apply.</li>
<li><b>UI_ANIMATION_DEPENDENCY_NONE</b> if nothing depends on the input.</li>
</ul>
For example, consider an interpolator (1) that accepts a final value as a parameter, (2) that always comes to a gradual stop at that final value, and (3) whose duration is determined by the difference between the final and initial values.  The interpolator should return <b>UI_ANIMATION_DEPENDENCY_INTERMEDIATE_VALUES</b>|<b>UI_ANIMATION_DURATION</b> for <i>initialValueDependencies</i>.  It should not return <b>UI_ANIMATION_DEPENDENCY_FINAL_VALUE</b> because this is set when the interpolator is created and is not affected by the initial value. Likewise it should not return <b>UI_ANIMATION_DEPENDENCY_FINAL_VELOCITY</b> because the slope of the curve is defined to always be zero when it reaches the final value.

It is important that an interpolator return correct set of flags. If a flag is not present for an output, Windows Animation assumes that the corresponding parameter does not affect that aspect of the interpolator's results.  For example, if the custom interpolator does not include <b>UI_ANIMATION_DEPENDENCY_FINAL_VALUE</b> for <i>initialVelocityDependencies</i>, Windows Animation may call <a href="https://msdn.microsoft.com/a1c5451a-b8d0-4eb7-883c-6bd1d585cb11">SetInitialValueAndVelocity</a> with an arbitrary velocity parameter, then call <a href="https://msdn.microsoft.com/5f99fc36-1f56-4275-9b6f-c22bde929d22">GetFinalValue</a> to determine the final value.  The interpolator's implementation of <b>GetFinalValue</b> must return the same result no matter what velocity parameter has been passed to <b>SetInitialValueAndVelocity</b> because the interpolator has claimed that the transition's final value does not depend on the initial velocity.

<div class="alert"><b>Note</b>  If the flags returned for <i>durationDependencies</i> do not include <b>UI_ANIMATION_DEPENDENCY_DURATION</b>, <a href="https://msdn.microsoft.com/79038ada-ebc2-4259-862a-d81403c2f6b8">SetDuration</a> will never be called on the interpolator.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc">
         IUIAnimationInterpolator</a>



<a href="https://msdn.microsoft.com/3620723e-5c9b-4d6a-8576-9017fa449a5d">UI_ANIMATION_DEPENDENCIES</a>
 

 

