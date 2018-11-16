---
UID: NN:uianimation.IUIAnimationInterpolator
title: IUIAnimationInterpolator
author: windows-sdk-content
description: Defines methods for creating a custom interpolator.
old-location: uianimation\iuianimationinterpolator.htm
tech.root: UIAnimation
ms.assetid: 8e1f2a9a-ab93-485a-83b2-baebb9ee4bcc
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IUIAnimationInterpolator, IUIAnimationInterpolator interface [Windows Animation], IUIAnimationInterpolator interface [Windows Animation],described, uianimation.iuianimationinterpolator, uianimation/IUIAnimationInterpolator
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
 - IUIAnimationInterpolator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationInterpolator interface


## -description


Defines methods for creating a custom interpolator.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationInterpolator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationInterpolator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationInterpolator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a897caa9-8a03-465e-8b74-b4614efce00c">GetDependencies</a>
</td>
<td align="left" width="63%">
Gets the aspects of the interpolator that depend on the initial value or velocity passed to <b>SetInitialValueAndVelocity</b>, or that depend on the duration passed to <b>SetDuration</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c39acf72-7c03-4d8b-b4f2-776e4b32f781">GetDuration</a>
</td>
<td align="left" width="63%">
Gets the duration of the transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f99fc36-1f56-4275-9b6f-c22bde929d22">GetFinalValue</a>
</td>
<td align="left" width="63%">
Gets the final value at the end of the transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f1cccd7-8b22-47a3-9704-0f22a1431c99">InterpolateValue</a>
</td>
<td align="left" width="63%">
Interpolates the value of an animation variable at the specified offset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae0b6674-307b-454e-b8be-db564c234607">InterpolateVelocity</a>
</td>
<td align="left" width="63%">
Interpolates the velocity, or rate of change, at the specified offset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79038ada-ebc2-4259-862a-d81403c2f6b8">SetDuration</a>
</td>
<td align="left" width="63%">
Sets the duration of the transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1c5451a-b8d0-4eb7-883c-6bd1d585cb11">SetInitialValueAndVelocity</a>
</td>
<td align="left" width="63%">
Sets the initial value and velocity at the start of the transition.

</td>
</tr>
</table> 


## -remarks



Client applications can use the transitions provided in  <a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a> or in a library provided by a third party; however, if you need custom behavior, you can create your own transitions by implementing the <b>IUIAnimationInterpolator</b> interface.

Before Windows Animation can use your custom interpolator, you must wrap it in an object that implements  <a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a> by calling the <a href="https://msdn.microsoft.com/02d28669-0cbd-41e2-b9ca-4ad893f09fc9">IUIAnimationTransitionFactory::CreateTransition</a> method and passing in the custom  interpolator.  After the interpolator is wrapped, client applications interact with your interpolator using the <b>IUIAnimationTransition</b> interface.

Custom interpolators can be reused across applications, but it is recommended that they be exposed using factory interfaces that return <a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a> interfaces.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/Dd940513(v=VS.85).aspx">Custom Interpolator Sample</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/62aec8da-e067-4b61-9465-e07fb5b42b7f">IUIAnimationTransitionFactory</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">IUIAnimationTransitionLibrary</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

