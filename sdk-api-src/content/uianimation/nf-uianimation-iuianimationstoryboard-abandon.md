---
UID: NF:uianimation.IUIAnimationStoryboard.Abandon
title: IUIAnimationStoryboard::Abandon
author: windows-sdk-content
description: Terminates the storyboard, releases all related animation variables, and removes the storyboard from the schedule.
old-location: uianimation\iuianimationstoryboard_abandon.htm
old-project: UIAnimation
ms.assetid: 2350dbd0-3a67-4832-94dd-56adce80a387
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: Abandon, Abandon method [Windows Animation], Abandon method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],Abandon method, IUIAnimationStoryboard.Abandon, IUIAnimationStoryboard::Abandon, uianimation.iuianimationstoryboard_abandon, uianimation/IUIAnimationStoryboard::Abandon
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationStoryboard.Abandon
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboard::Abandon


## -description


Terminates the storyboard, releases all related animation variables, and removes the storyboard from the schedule.


## -parameters






## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks




         This method can be called before or after the storyboard starts playing.

This method does not trigger any storyboard events.




## -see-also




<a href="https://msdn.microsoft.com/cecb0026-ed6f-48b8-9381-d020a36e7e87">
      IUIAnimationManager::AbandonAllStoryboards</a>



<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/82f915df-c031-41e9-8347-044b37793182">
      IUIAnimationStoryboard::Conclude</a>



<a href="https://msdn.microsoft.com/45d0872a-dbcf-4151-a880-80b2c6fb884c">IUIAnimationStoryboard::Finish</a>



<a href="https://msdn.microsoft.com/b47d4ffd-ae51-40e7-8f91-9d7b7b2901c8">
      IUIAnimationStoryboard::Schedule</a>
 

 

