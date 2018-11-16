---
UID: NN:uianimation.IUIAnimationVariable
title: IUIAnimationVariable
author: windows-sdk-content
description: Defines an animation variable, which represents a visual element that can be animated.
old-location: uianimation\iuianimationvariable.htm
tech.root: UIAnimation
ms.assetid: 1632e62d-6e82-4841-8823-f6b60efc4298
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IUIAnimationVariable, IUIAnimationVariable interface [Windows Animation], IUIAnimationVariable interface [Windows Animation],described, uianimation.iuianimationvariable, uianimation/IUIAnimationVariable
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
 - IUIAnimationVariable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationVariable interface


## -description


Defines an animation variable, which represents a visual element that can be animated.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationVariable</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationVariable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationVariable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56042549-d6f6-4eed-8079-c1b14acbe160">GetCurrentStoryboard</a>
</td>
<td align="left" width="63%">
Gets the storyboard that is currently animating the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19d71abc-e3f8-48d4-9ceb-5920dcc9c007">GetFinalIntegerValue</a>
</td>
<td align="left" width="63%">
Gets the final value of the animation variable as an integer.      
         

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/577f83c1-aba7-4a51-82dc-68a103a31377">GetFinalValue</a>
</td>
<td align="left" width="63%">
Gets the final value of the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/044fd6a3-6e40-4f4f-8777-1a1a66c91989">GetIntegerValue</a>
</td>
<td align="left" width="63%">
Gets the current value of the animation variable as an integer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccf4c575-aa98-40cd-b2de-cf8db95ec57d">GetPreviousIntegerValue</a>
</td>
<td align="left" width="63%">
Gets the previous value of the animation variable as an integer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/405bc35e-8b38-40fb-acf4-107fa6dd161a">GetPreviousValue</a>
</td>
<td align="left" width="63%">
Gets the previous value of the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2731d302-dc52-4a10-8012-a246856d132b">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag for an animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51ae200a-a630-44fd-afd4-33d1b1dbf6d7">GetValue</a>
</td>
<td align="left" width="63%">
Gets the current value of the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e8f1106-6320-4670-867a-24ce6597026e">SetLowerBound</a>
</td>
<td align="left" width="63%">
Sets the lower bound (floor) for the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8c86195-14a1-4535-9fc2-4992c8090e79">SetRoundingMode</a>
</td>
<td align="left" width="63%">
Specifies the rounding mode for the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/176b0047-cac8-474b-9126-fdab4bc41537">SetTag</a>
</td>
<td align="left" width="63%">
Sets the tag for an animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d202f453-2e69-415b-823c-5a3279722274">SetUpperBound</a>
</td>
<td align="left" width="63%">
Sets the upper bound (ceiling) for the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d773a59f-10a5-41e4-92f1-af72d8d15105">SetVariableChangeHandler</a>
</td>
<td align="left" width="63%">
Specifies a variable change handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8dc20701-0808-4308-92fc-8be6c4b039ca">SetVariableIntegerChangeHandler</a>
</td>
<td align="left" width="63%">
Specifies an integer variable change handler.

</td>
</tr>
</table> 


## -remarks



Along with 
         <a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">IUIAnimationTransition</a> and 
         <a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>, <b>IUIAnimationVariable</b> is a primary component for building animations. To create and manage animation variables, use <a href="https://msdn.microsoft.com/21f16c65-90aa-4b1f-93bc-8ee0488c6ded">IUIAnimationManager</a>.




## -see-also




<a href="https://msdn.microsoft.com/e4c38e78-1b9e-4918-ba15-6a4c5c390c07">IUIAnimationManager::CreateAnimationVariable</a>



<a href="https://msdn.microsoft.com/611c5341-f225-461d-9718-a2432d796764">IUIAnimationManager::GetVariableFromTag</a>



<a href="https://msdn.microsoft.com/0178b674-2ad3-49ee-92ce-925840ab8409">IUIAnimationManager::ScheduleTransition</a>



<a href="https://msdn.microsoft.com/c3213e5d-c8f5-406a-bc44-9de7a740b070">IUIAnimationStoryboard::AddTransition</a>



<a href="https://msdn.microsoft.com/94a9aafc-fe5a-49a8-8e14-9e7c4624869a">IUIAnimationStoryboard::AddTransitionAtKeyframe</a>



<a href="https://msdn.microsoft.com/75db41ef-526b-40aa-a62d-a4262cc8d80e">IUIAnimationStoryboard::AddTransitionBetweenKeyframes</a>



<a href="https://msdn.microsoft.com/ac5ee9c0-cecb-41f1-b8d3-6f779dfafef7">IUIAnimationStoryboard::HoldVariable</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

