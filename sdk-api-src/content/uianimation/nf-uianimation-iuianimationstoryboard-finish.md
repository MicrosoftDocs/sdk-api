---
UID: NF:uianimation.IUIAnimationStoryboard.Finish
title: IUIAnimationStoryboard::Finish
author: windows-sdk-content
description: Finishes the storyboard within the specified time, compressing the storyboard if necessary.
old-location: uianimation\iuianimationstoryboard_finish.htm
old-project: UIAnimation
ms.assetid: 45d0872a-dbcf-4151-a880-80b2c6fb884c
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: Finish, Finish method [Windows Animation], Finish method [Windows Animation],IUIAnimationStoryboard interface, IUIAnimationStoryboard interface [Windows Animation],Finish method, IUIAnimationStoryboard.Finish, IUIAnimationStoryboard::Finish, uianimation.iuianimationstoryboard_finish, uianimation/IUIAnimationStoryboard::Finish
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
 - IUIAnimationStoryboard.Finish
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboard::Finish


## -description


Finishes the storyboard within the specified time, compressing the storyboard if necessary.


## -parameters




### -param completionDeadline [in]


                The maximum amount of time that the storyboard can use to finish playing.


## -returns




            If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method has no effect on storyboard events. Events continue to be raised as expected while the storyboard plays.




## -see-also




<a href="https://msdn.microsoft.com/db5ba70c-3904-4053-881a-b1412beb35f3">
      IUIAnimationManager::FinishAllStoryboards</a>



<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/2350dbd0-3a67-4832-94dd-56adce80a387">
      IUIAnimationStoryboard::Abandon</a>



<a href="https://msdn.microsoft.com/82f915df-c031-41e9-8347-044b37793182">
      IUIAnimationStoryboard::Conclude</a>



<a href="https://msdn.microsoft.com/b47d4ffd-ae51-40e7-8f91-9d7b7b2901c8">
      IUIAnimationStoryboard::Schedule</a>
 

 

