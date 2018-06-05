---
UID: NF:uianimation.IUIAnimationManager.Resume
title: IUIAnimationManager::Resume
author: windows-sdk-content
description: Resumes all animations.
old-location: uianimation\iuianimationmanager_resume.htm
old-project: UIAnimation
ms.assetid: f29a9337-0ed0-46f8-ab77-8f82ab39d8df
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUIAnimationManager interface [Windows Animation],Resume method, IUIAnimationManager.Resume, IUIAnimationManager::Resume, Resume, Resume method [Windows Animation], Resume method [Windows Animation],IUIAnimationManager interface, uianimation.iuianimationmanager_resume, uianimation/IUIAnimationManager::Resume
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
tech.root: 
req.typenames: UI_ANIMATION_TIMER_CLIENT_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAnimation.dll
api_name:
-	IUIAnimationManager.Resume
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationManager::Resume


## -description



      Resumes all animations.


## -parameters






## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks




         When an animation manager is resumed, and at least one animation is currently scheduled or playing, its status is set to <b>UI_ANIMATION_MANAGER_BUSY</b>.




## -see-also




<a href="https://msdn.microsoft.com/21f16c65-90aa-4b1f-93bc-8ee0488c6ded">IUIAnimationManager</a>



<a href="https://msdn.microsoft.com/838140c3-12ca-4909-a0f8-713b5472e5a9">
      IUIAnimationManager::GetStatus</a>



<a href="https://msdn.microsoft.com/52b11e79-9930-4fd8-84b4-152917090519">
      IUIAnimationManager::Pause</a>



<a href="https://msdn.microsoft.com/499c74c0-d1e7-4ab4-9c3a-19c2e1abeda8">
      UI_ANIMATION_MANAGER_STATUS</a>
 

 

