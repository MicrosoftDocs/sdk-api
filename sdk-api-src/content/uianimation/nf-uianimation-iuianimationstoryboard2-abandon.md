---
UID: NF:uianimation.IUIAnimationStoryboard2.Abandon
title: IUIAnimationStoryboard2::Abandon
author: windows-driver-content
description: Terminates the storyboard, releases all related animation variables, and removes the storyboard from the schedule.
old-location: uianimation\iuianimationstoryboard2_abandon.htm
old-project: UIAnimation
ms.assetid: ABB7184F-A703-45E3-96D8-E3062EEB9565
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: Abandon, Abandon method [Windows Animation], Abandon method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],Abandon method, IUIAnimationStoryboard2.Abandon, IUIAnimationStoryboard2::Abandon, uianimation.iuianimationstoryboard2_abandon, uianimation/IUIAnimationStoryboard2::Abandon
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps | UWP apps]
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
-	IUIAnimationStoryboard2.Abandon
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboard2::Abandon


## -description


Terminates the storyboard, releases all related animation variables, and removes the storyboard from the schedule.


## -parameters






## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks




         This method can be called before or after the storyboard starts playing.

This method does not trigger any storyboard events.




## -see-also




<a href="https://msdn.microsoft.com/E8DC71C0-CA68-4FD8-81CE-68450BF4EBA7">
      IUIAnimationManager2::AbandonAllStoryboards</a>



<a href="https://msdn.microsoft.com/507B6C2B-92C6-4AEB-82D5-3F14A332D41F">IUIAnimationStoryboard2</a>



<a href="https://msdn.microsoft.com/C7687E52-433F-4E73-910D-86298E528F7B">
      IUIAnimationStoryboard2::Conclude</a>



<a href="https://msdn.microsoft.com/632BC77D-F2C5-4D08-8E9C-0598617A1DA7">IUIAnimationStoryboard2::Finish</a>



<a href="https://msdn.microsoft.com/9F20AE4A-F693-4DDA-90F4-FCCA5291208B">
      IUIAnimationStoryboard2::Schedule</a>
 

 

