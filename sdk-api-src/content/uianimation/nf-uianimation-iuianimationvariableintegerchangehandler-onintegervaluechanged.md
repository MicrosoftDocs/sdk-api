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

# IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged


## -description



      Handles events that occur when the value of an animation variable changes.

This method receives updates as <b>INT32</b> values. To receive updates as <b>DOUBLE</b> values, use the <a href="https://msdn.microsoft.com/1e865f55-d703-4d91-8690-b816b5fe1a89">IUIAnimationVariableChangeHandler::OnValueChanged</a> method.


## -parameters




### -param storyboard [in]


            The storyboard that is animating the animation variable  specified by the <i>variable</i> parameter.


### -param variable [in]


             The animation variable that has been updated.


### -param newValue [in]


            The new value of the animation variable, rounded according to the variable's rounding mode.


### -param previousValue [in]


            The previous value of the animation variable, rounded according to the variable's rounding mode.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



The rounding mode for an animation variable is specified using the <a href="https://msdn.microsoft.com/e8c86195-14a1-4535-9fc2-4992c8090e79">IUIAnimationVariable::SetRoundingMode</a> method.

<b>OnIntegerValueChanged</b> events might occur less frequently than <a href="https://msdn.microsoft.com/1e865f55-d703-4d91-8690-b816b5fe1a89">OnValueChanged</a> events because values such as 2.2, 2.3, 2.4 would all be rounded to the same integer.

By default, a call made in a callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>. However, there are exceptions to this default. The following methods can be successfully called from <b>OnIntegerValueChanged</b>:

<ul>
<li>
<a href="https://msdn.microsoft.com/56042549-d6f6-4eed-8079-c1b14acbe160">IUIAnimationVariable::GetCurrentStoryboard</a>
</li>
<li>
<a href="https://msdn.microsoft.com/19d71abc-e3f8-48d4-9ceb-5920dcc9c007">IUIAnimationVariable::GetFinalIntegerValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/577f83c1-aba7-4a51-82dc-68a103a31377">IUIAnimationVariable::GetFinalValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/044fd6a3-6e40-4f4f-8777-1a1a66c91989">IUIAnimationVariable::GetIntegerValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ccf4c575-aa98-40cd-b2de-cf8db95ec57d">IUIAnimationVariable::GetPreviousIntegerValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/405bc35e-8b38-40fb-acf4-107fa6dd161a">IUIAnimationVariable::GetPreviousValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/51ae200a-a630-44fd-afd4-33d1b1dbf6d7">IUIAnimationVariable::GetValue</a>
</li>
<li>
<a href="https://msdn.microsoft.com/74a9265a-3602-4707-949e-6073cbde9ac4">IUIAnimationManager::GetStoryboardFromTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/611c5341-f225-461d-9718-a2432d796764">IUIAnimationManager::GetVariableFromTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9c74dc23-ea42-400d-a78c-79b716c5e614">IUIAnimationStoryboard::GetTag</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2731d302-dc52-4a10-8012-a246856d132b">IUIAnimationVariable::GetTag</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/044fd6a3-6e40-4f4f-8777-1a1a66c91989">
      IUIAnimationVariable::GetIntegerValue</a>



<a href="https://msdn.microsoft.com/ccf4c575-aa98-40cd-b2de-cf8db95ec57d">
      IUIAnimationVariable::GetPreviousIntegerValue</a>



<a href="https://msdn.microsoft.com/e8c86195-14a1-4535-9fc2-4992c8090e79">IUIAnimationVariable::SetRoundingMode</a>



<a href="https://msdn.microsoft.com/8dc20701-0808-4308-92fc-8be6c4b039ca">IUIAnimationVariable::SetVariableIntegerChangeHandler</a>



<a href="https://msdn.microsoft.com/1e865f55-d703-4d91-8690-b816b5fe1a89">IUIAnimationVariableChangeHandler::OnValueChanged</a>



<a href="https://msdn.microsoft.com/acd9ff0f-e2e4-4711-9d9c-54624f170ec6">IUIAnimationVariableIntegerChangeHandler</a>



<a href="https://msdn.microsoft.com/0221207b-4583-44b8-85aa-dc6cd4cd9d25">UI_ANIMATION_ROUNDING_MODE </a>
 

 

