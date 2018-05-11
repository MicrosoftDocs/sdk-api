---
UID: NF:uianimation.IUIAnimationStoryboard2.HoldVariable
title: IUIAnimationStoryboard2::HoldVariable
author: windows-driver-content
description: Directs the storyboard to hold the specified animation variable at its final value until the storyboard ends.
old-location: uianimation\iuianimationstoryboard2_holdvariable.htm
old-project: UIAnimation
ms.assetid: E6B7C4F9-2377-4968-A16F-15F174EC5439
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: HoldVariable, HoldVariable method [Windows Animation], HoldVariable method [Windows Animation],IUIAnimationStoryboard2 interface, IUIAnimationStoryboard2 interface [Windows Animation],HoldVariable method, IUIAnimationStoryboard2.HoldVariable, IUIAnimationStoryboard2::HoldVariable, uianimation.iuianimationstoryboard2_holdvariable, uianimation/IUIAnimationStoryboard2::HoldVariable
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
-	IUIAnimationStoryboard2.HoldVariable
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboard2::HoldVariable


## -description



      Directs the storyboard to hold the specified animation variable at its final value until the storyboard ends.


## -parameters




### -param variable [in]


            The animation variable.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks




         When a storyboard is playing, it has exclusive access to any variables it animates unless the storyboard is trimmed by a higher-priority storyboard. Typically, this exclusive access is released  when the last transition in the storyboard for that variable finishes playing. Applications can call this method to maintain exclusive access to the animation variable and hold the variable, at the final value of the last transition, until the end of the storyboard.




## -see-also




<a href="https://msdn.microsoft.com/507B6C2B-92C6-4AEB-82D5-3F14A332D41F">IUIAnimationStoryboard2</a>



<a href="https://msdn.microsoft.com/A676EF27-B59D-4D2D-AD5B-8F46EE337E69">IUIAnimationVariable2</a>
 

 

