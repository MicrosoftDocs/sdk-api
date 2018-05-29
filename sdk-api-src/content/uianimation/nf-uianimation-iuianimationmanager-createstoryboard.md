---
UID: NF:uianimation.IUIAnimationManager.CreateStoryboard
title: IUIAnimationManager::CreateStoryboard
author: windows-sdk-content
description: Creates a new storyboard.
old-location: uianimation\iuianimationmanager_createstoryboard.htm
old-project: UIAnimation
ms.assetid: 933ffb62-0f69-4225-873b-e2e023939bea
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CreateStoryboard, CreateStoryboard method [Windows Animation], CreateStoryboard method [Windows Animation],IUIAnimationManager interface, IUIAnimationManager interface [Windows Animation],CreateStoryboard method, IUIAnimationManager.CreateStoryboard, IUIAnimationManager::CreateStoryboard, uianimation.iuianimationmanager_createstoryboard, uianimation/IUIAnimationManager::CreateStoryboard
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
-	IUIAnimationManager.CreateStoryboard
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationManager::CreateStoryboard


## -description



      Creates a new storyboard.


## -parameters




### -param storyboard [out]


               The new storyboard.


## -returns




                
            If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Storyboards can specify complex coordinated updates to many animation variables. These updates happen in sequence or in parallel, and they are guaranteed to remain synchronized within the storyboard. A storyboard is created, populated with transitions on animation variables, and then scheduled. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/e2641c93-e520-4749-a98e-5a58c175fdb9">Create a Storyboard and Add Transitions</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/21f16c65-90aa-4b1f-93bc-8ee0488c6ded">IUIAnimationManager</a>



<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">
      IUIAnimationStoryboard</a>
 

 

