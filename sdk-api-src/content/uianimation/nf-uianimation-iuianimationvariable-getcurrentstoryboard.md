---
UID: NF:uianimation.IUIAnimationVariable.GetCurrentStoryboard
title: IUIAnimationVariable::GetCurrentStoryboard
author: windows-sdk-content
description: Gets the storyboard that is currently animating the animation variable.
old-location: uianimation\iuianimationvariable_getcurrentstoryboard.htm
old-project: UIAnimation
ms.assetid: 56042549-d6f6-4eed-8079-c1b14acbe160
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetCurrentStoryboard, GetCurrentStoryboard method [Windows Animation], GetCurrentStoryboard method [Windows Animation],IUIAnimationVariable interface, IUIAnimationVariable interface [Windows Animation],GetCurrentStoryboard method, IUIAnimationVariable.GetCurrentStoryboard, IUIAnimationVariable::GetCurrentStoryboard, uianimation.iuianimationvariable_getcurrentstoryboard, uianimation/IUIAnimationVariable::GetCurrentStoryboard
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
 - IUIAnimationVariable.GetCurrentStoryboard
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationVariable::GetCurrentStoryboard


## -description


Gets the storyboard that is currently animating the animation variable.


## -parameters




### -param storyboard [out]

The current storyboard, or <b>NULL</b> if no storyboard is currently animating the animation variable.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">UIAnimation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/1632e62d-6e82-4841-8823-f6b60efc4298">IUIAnimationVariable</a>
 

 

