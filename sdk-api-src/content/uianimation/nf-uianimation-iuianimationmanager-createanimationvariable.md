---
UID: NF:uianimation.IUIAnimationManager.CreateAnimationVariable
title: IUIAnimationManager::CreateAnimationVariable
author: windows-sdk-content
description: Creates a new animation variable.
old-location: uianimation\iuianimationmanager_createanimationvariable.htm
old-project: UIAnimation
ms.assetid: e4c38e78-1b9e-4918-ba15-6a4c5c390c07
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreateAnimationVariable, CreateAnimationVariable method [Windows Animation], CreateAnimationVariable method [Windows Animation],IUIAnimationManager interface, IUIAnimationManager interface [Windows Animation],CreateAnimationVariable method, IUIAnimationManager.CreateAnimationVariable, IUIAnimationManager::CreateAnimationVariable, uianimation.iuianimationmanager_createanimationvariable, uianimation/IUIAnimationManager::CreateAnimationVariable
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
 - IUIAnimationManager.CreateAnimationVariable
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationManager::CreateAnimationVariable


## -description


Creates a new animation variable.


## -parameters




### -param initialValue [in]

The initial value for the new animation variable.


### -param variable [out]

The new animation variable.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



The initial value of an animation variable is specified when the variable is created. After an animation variable is created, its value cannot be changed directly; it must be updated through the animation manager.

An animation variable is typically created to represent each visual characteristic that is to be animated. For example, an application might create two animation variables for the X and Y coordinates of an object that can move freely within a window.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/360aa157-cb50-400a-b373-45885410469d">Create Animation Variables</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/21f16c65-90aa-4b1f-93bc-8ee0488c6ded">IUIAnimationManager</a>



<a href="https://msdn.microsoft.com/1632e62d-6e82-4841-8823-f6b60efc4298">IUIAnimationVariable</a>
 

 

