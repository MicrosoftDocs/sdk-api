---
UID: NF:uianimation.IUIAnimationVariable.SetRoundingMode
title: IUIAnimationVariable::SetRoundingMode
author: windows-sdk-content
description: Specifies the rounding mode for the animation variable.
old-location: uianimation\iuianimationvariable_setroundingmode.htm
old-project: UIAnimation
ms.assetid: e8c86195-14a1-4535-9fc2-4992c8090e79
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IUIAnimationVariable interface [Windows Animation],SetRoundingMode method, IUIAnimationVariable.SetRoundingMode, IUIAnimationVariable::SetRoundingMode, SetRoundingMode, SetRoundingMode method [Windows Animation], SetRoundingMode method [Windows Animation],IUIAnimationVariable interface, uianimation.iuianimationvariable_setroundingmode, uianimation/IUIAnimationVariable::SetRoundingMode
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
 - IUIAnimationVariable.SetRoundingMode
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationVariable::SetRoundingMode


## -description


Specifies the rounding mode for the animation variable.


## -parameters




### -param mode [in]

The rounding mode for the animation variable.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



An animation variable's rounding mode determines how a floating-point value is converted to an integer.
      The default mode for each variable is <b>UI_ANIMATION_ROUNDING_NEAREST</b>.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/360aa157-cb50-400a-b373-45885410469d">Create Animation Variables</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1632e62d-6e82-4841-8823-f6b60efc4298">IUIAnimationVariable</a>



<a href="https://msdn.microsoft.com/19d71abc-e3f8-48d4-9ceb-5920dcc9c007">IUIAnimationVariable::GetFinalIntegerValue</a>



<a href="https://msdn.microsoft.com/044fd6a3-6e40-4f4f-8777-1a1a66c91989">IUIAnimationVariable::GetIntegerValue</a>



<a href="https://msdn.microsoft.com/ccf4c575-aa98-40cd-b2de-cf8db95ec57d">IUIAnimationVariable::GetPreviousIntegerValue</a>



<a href="https://msdn.microsoft.com/0221207b-4583-44b8-85aa-dc6cd4cd9d25">UI_ANIMATION_ROUNDING_MODE</a>
 

 

