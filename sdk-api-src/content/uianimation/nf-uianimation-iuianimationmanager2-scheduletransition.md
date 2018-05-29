---
UID: NF:uianimation.IUIAnimationManager2.ScheduleTransition
title: IUIAnimationManager2::ScheduleTransition
author: windows-sdk-content
description: Creates and schedules a single-transition storyboard.
old-location: uianimation\iuianimationmanager2_scheduletransition.htm
old-project: UIAnimation
ms.assetid: F0F5D099-6290-485F-AD68-101CD57E8656
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],ScheduleTransition method, IUIAnimationManager2.ScheduleTransition, IUIAnimationManager2::ScheduleTransition, ScheduleTransition, ScheduleTransition method [Windows Animation], ScheduleTransition method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_scheduletransition, uianimation/IUIAnimationManager2::ScheduleTransition
ms.prod: windows
ms.technology: windows-sdk
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
-	IUIAnimationManager2.ScheduleTransition
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationManager2::ScheduleTransition


## -description



      Creates and schedules a single-transition storyboard.


## -parameters




### -param variable [in]


                The animation variable.


### -param transition [in]


               A transition to be applied to the animation variable.


### -param timeNow [in]


               The current system time.


## -returns



Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method schedules a new storyboard by creating the storyboard, applying the specified transition to the specified variable, and then scheduling the storyboard.




## -see-also




<a href="https://msdn.microsoft.com/BD7DAD23-2A7D-4EE7-9BCF-8380F928674D">IUIAnimationManager2</a>



<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/507B6C2B-92C6-4AEB-82D5-3F14A332D41F">IUIAnimationStoryboard2</a>



<a href="https://msdn.microsoft.com/32654e4b-158b-4d1a-afc7-98f90212b33b">
      IUIAnimationTimer::GetTime</a>



<a href="https://msdn.microsoft.com/99804a2f-82c9-494c-b75d-69e66f1e49ef">
      IUIAnimationTransition</a>



<a href="https://msdn.microsoft.com/CACB8053-7716-42E4-9C3B-9CCBBC30808A">
      IUIAnimationTransition2</a>



<a href="https://msdn.microsoft.com/7d256937-b191-499f-9711-05a5ef3b8e18">
      IUIAnimationTransitionLibrary</a>



<a href="https://msdn.microsoft.com/92C10ED5-DCE6-4B1D-8608-E2C3C6AD97BA">
      IUIAnimationTransitionLibrary2</a>



<a href="https://msdn.microsoft.com/1632e62d-6e82-4841-8823-f6b60efc4298">
      IUIAnimationVariable</a>



<a href="https://msdn.microsoft.com/A676EF27-B59D-4D2D-AD5B-8F46EE337E69">
      IUIAnimationVariable2</a>
 

 

