---
UID: NN:uianimation.IUIAnimationInterpolator2
title: IUIAnimationInterpolator2
author: windows-driver-content
description: Extends the IUIAnimationInterpolator interface that defines methods for creating a custom interpolator. IUIAnimationInterpolator2 supports interpolation in a given dimension.
old-location: uianimation\iuianimationinterpolator2.htm
old-project: UIAnimation
ms.assetid: EC0D1933-37C3-41E2-AB13-DA4AAF4B8F04
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IUIAnimationInterpolator2, IUIAnimationInterpolator2 interface [Windows Animation], IUIAnimationInterpolator2 interface [Windows Animation],described, uianimation.iuianimationinterpolator2, uianimation/IUIAnimationInterpolator2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
-	IUIAnimationInterpolator2
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationInterpolator2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc">IUIAnimationInterpolator</a> interface that defines methods for creating a custom interpolator.   <b>IUIAnimationInterpolator2</b> supports interpolation in a given dimension. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationInterpolator2</b> interface inherits from <a href="https://msdn.microsoft.com/8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc">IUIAnimationInterpolator</a>. <b>IUIAnimationInterpolator2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationInterpolator2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DC6F046E-1A35-4FB9-9016-853AF2B598DE">GetDependencies</a>
</td>
<td align="left" width="63%">
For the given dimension, <a href="https://msdn.microsoft.com/DC6F046E-1A35-4FB9-9016-853AF2B598DE">GetDependencies</a> retrieves the aspects of the interpolator that depend on the initial value or velocity that is passed to the <a href="https://msdn.microsoft.com/F1C0C54D-86C3-4B65-96A4-66D89F2B2084">IUIAnimationInterpolator2::SetInitialValueAndVelocity</a> method or the duration that is passed to the <a href="https://msdn.microsoft.com/C1E6EC87-283A-4C56-96C5-531C5C5F5575">IUIAnimationInterpolator2::SetDuration</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66CA3AE5-4332-42CC-BD38-A5F19F0F3C89">GetDimension</a>
</td>
<td align="left" width="63%">
Gets the number of dimensions that require interpolation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/962FAF0A-CFA9-4F0D-AADC-75B42E788151">GetDuration</a>
</td>
<td align="left" width="63%">
Gets the duration of a transition for the given dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/330816C7-1641-41FA-8FB9-56FCE0108593">GetFinalValue</a>
</td>
<td align="left" width="63%">
Gets the final value at the end of the transition for the given dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E3CE4D97-08C8-46F4-B8B0-42CA4212DF50">GetPrimitiveInterpolation</a>
</td>
<td align="left" width="63%">
Generates a primitive interpolation of the specified animation curve.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A512B264-642A-4E4B-9AEA-DE80B9D99A53">InterpolateValue</a>
</td>
<td align="left" width="63%">
Interpolates the value of an animation variable at the specified offset and for the given dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B6BD1B9D-3553-4A83-BB57-629611F9CA18">InterpolateVelocity</a>
</td>
<td align="left" width="63%">
Interpolates the velocity, or rate of change, at the specified offset for the given dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C1E6EC87-283A-4C56-96C5-531C5C5F5575">SetDuration</a>
</td>
<td align="left" width="63%">
Sets the duration of the transition in the given dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F1C0C54D-86C3-4B65-96A4-66D89F2B2084">SetInitialValueAndVelocity</a>
</td>
<td align="left" width="63%">
Sets the initial value and velocity of the transition for the given dimension.

</td>
</tr>
</table> 


## -remarks



Client applications can use the transitions provided in  the <a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a> or<a href="https://msdn.microsoft.com/92C10ED5-DCE6-4B1D-8608-E2C3C6AD97BA">IUIAnimationTransitionLibrary2</a> interfaces, or in a library provided by a third party; however, custom transitions can be created by implementing the <a href="https://msdn.microsoft.com/8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc">IUIAnimationInterpolator</a> or  <b>IUIAnimationInterpolator2</b> interfaces.

Before Windows Animation can use your custom interpolator, you must wrap it in an object that implements the  <a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a> interface (by calling <a href="https://msdn.microsoft.com/02d28669-0cbd-41e2-b9ca-4ad893f09fc9">IUIAnimationTransitionFactory::CreateTransition</a>) or the <a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">IUIAnimationTransition2</a> interface (by calling  <a href="https://msdn.microsoft.com/EB829B6A-770C-486A-9BA2-4D7C8F073C8F">IUIAnimationTransitionFactory2::CreateTransition</a>)  and passing in the custom  interpolator.  After the interpolator wrapper has been created, client applications interact with your interpolator using the <b>IUIAnimationTransition</b> or <b>IUIAnimationTransition2</b> interfaces.

Custom interpolators can be reused across applications, but it is recommended that they be exposed using factory interfaces that return an  <a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a> interface or an <a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">IUIAnimationTransition2</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc">IUIAnimationInterpolator</a>



<a href="https://msdn.microsoft.com/6EAE7874-1103-4D2E-A325-37E5A95705F5">IUIAnimationPrimitiveInterpolation</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

