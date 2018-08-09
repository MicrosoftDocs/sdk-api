---
UID: NN:uianimation.IUIAnimationVariable2
title: IUIAnimationVariable2
author: windows-sdk-content
description: Defines an animation variable, which represents a visual element that can be animated in multiple dimensions.
old-location: uianimation\iuianimationvariable2.htm
old-project: UIAnimation
ms.assetid: A676EF27-B59D-4D2D-AD5B-8F46EE337E69
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IUIAnimationVariable2, IUIAnimationVariable2 interface [Windows Animation], IUIAnimationVariable2 interface [Windows Animation],described, uianimation.iuianimationvariable2, uianimation/IUIAnimationVariable2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps \| UWP apps]
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
 - IUIAnimationVariable2
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationVariable2 interface


## -description


Defines an animation variable, which represents a visual element that can be animated in multiple dimensions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationVariable2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationVariable2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationVariable2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7A9B4A84-94E4-4B6C-B2FF-0A0A70397D21">GetCurrentStoryboard</a>
</td>
<td align="left" width="63%">
Gets the active storyboard for the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59E7C7A1-2461-487C-A263-A9DFC851B720">GetCurve</a>
</td>
<td align="left" width="63%">
Gets the animation curve of the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/572C3851-88CD-44FE-A842-62DBD3994CB6">GetDimension</a>
</td>
<td align="left" width="63%">
Gets the number of dimensions that the animation variable is to be animated in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/290EC1D8-007D-44A0-B3F8-384A9594FDC4">GetFinalIntegerValue</a>
</td>
<td align="left" width="63%">
Gets the final integer value of the animation variable. This is the value after all currently scheduled animations have completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/191DA982-E3F1-4E37-A4D8-7813201E6B6B">GetFinalIntegerVectorValue</a>
</td>
<td align="left" width="63%">
Gets the final integer value of the animation variable for the specified dimension. This is the value after all currently scheduled animations have completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FF39BE67-AED7-4B67-ABAF-D5D51619F0D3">GetFinalValue</a>
</td>
<td align="left" width="63%">
Gets the final value of the animation variable. This is the value after all currently scheduled animations have completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2794B65F-0461-4E0F-832D-CEC9BEE60B6E">GetFinalVectorValue</a>
</td>
<td align="left" width="63%">
Gets the final value of the animation variable for the specified dimension. This is the value after all currently scheduled animations have completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C878B86A-87AD-457A-802A-9A329B401B08">GetIntegerValue</a>
</td>
<td align="left" width="63%">
Gets the integer value of the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63832D4C-C1AB-4073-AE36-1539671F0F59">GetIntegerVectorValue</a>
</td>
<td align="left" width="63%">
Gets the integer value of the animation variable for the specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8B25BE8D-B12F-44B4-AFBF-3E6994BA0771">GetPreviousIntegerValue</a>
</td>
<td align="left" width="63%">
Gets the previous integer value of the animation variable in the specified dimension. This is the value of the animation variable before the most recent update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7061B16A-FB54-4274-8425-551396F353CF">GetPreviousIntegerVectorValue</a>
</td>
<td align="left" width="63%">
Gets the previous integer value of the animation variable for the specified dimension. This is the value of the animation variable before the most recent update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1A2BF7DB-1C7B-43BF-A7F7-A4FB47250597">GetPreviousValue</a>
</td>
<td align="left" width="63%">
Gets the previous value of the animation variable. This is the value of the animation variable before the most recent update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E6C32B28-A6DE-47FB-8399-CA0B782D8B25">GetPreviousVectorValue</a>
</td>
<td align="left" width="63%">
Gets the previous value of the animation variable for the specified dimension. This is the value of the animation variable before the most recent update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29E6CA4D-527D-4C9D-9E28-2E2C67516126">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag of the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597624">GetValue</a>
</td>
<td align="left" width="63%">
Gets the value of the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CAC7D415-5B0F-4587-8F1C-65399D2A5A58">GetVectorCurve</a>
</td>
<td align="left" width="63%">
Gets the animation curve of the animation variable for the specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B53EDC6C-7B1E-4CDE-8F4A-5B0601892630">GetVectorValue</a>
</td>
<td align="left" width="63%">
Gets the value of the animation variable in the specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5149778F-C78D-49C2-8C2E-DBAB00B78DE8">SetLowerBound</a>
</td>
<td align="left" width="63%">
Sets the lower bound (floor) for the value of the animation variable. The value of the animation variable should not fall below the specified value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CB7D30BF-D22C-40EB-A530-035CED1BDAF0">SetLowerBoundVector</a>
</td>
<td align="left" width="63%">
Sets the lower bound (floor) value of each specified dimension for the animation variable. The value of each animation variable should not fall below its lower bound.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D2FCC17B-0584-4317-8BD7-25454E4A553C">SetRoundingMode</a>
</td>
<td align="left" width="63%">
Sets the rounding mode of the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21BAFF23-8866-432F-BB9A-0328CE0E6021">SetTag</a>
</td>
<td align="left" width="63%">
Sets the tag of the animation variable.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AE142CD9-61BB-427A-A40B-42EFDD0B5CAD">SetUpperBound</a>
</td>
<td align="left" width="63%">
Sets the upper bound (ceiling) for the value of the animation variable. The value of the animation variable should not rise above the specified value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/776CDF6F-F93F-44DC-93D7-79D3A866FAF2">SetUpperBoundVector</a>
</td>
<td align="left" width="63%">
Sets the upper bound (ceiling) value of each specified dimension for the animation variable. The value of each animation variable should not rise above its upper bound.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F603C693-8F91-483F-8B0A-712E03BC10E5">SetVariableChangeHandler</a>
</td>
<td align="left" width="63%">
Specifies a handler for changes to the value of the animation variable. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98C95C85-30C9-4E3E-82FE-E3D4C7ECAE0B">SetVariableCurveChangeHandler</a>
</td>
<td align="left" width="63%">
Specifies a handler for changes to the animation curve of the animation variable. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4327AC4A-2C2C-4C1A-AFCD-D2BA8ECEBA12">SetVariableIntegerChangeHandler</a>
</td>
<td align="left" width="63%">
Specifies a handler for changes to the integer value of the animation variable. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

