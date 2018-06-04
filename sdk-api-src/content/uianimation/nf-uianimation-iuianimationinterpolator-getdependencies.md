---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

