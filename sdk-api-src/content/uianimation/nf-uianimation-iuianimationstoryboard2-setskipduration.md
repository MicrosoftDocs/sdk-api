---
UID: NF:uianimation.IUIAnimationStoryboard2.SetSkipDuration
title: IUIAnimationStoryboard2::SetSkipDuration
author: windows-driver-content
description: Specifies an offset from the beginning of a storyboard at which to start animating.
old-location: uianimation\iuianimationstoryboard2_setskipduration.htm
old-project: UIAnimation
ms.assetid: 177623D7-5516-41EA-9014-61B150E527D9
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IUIAnimationStoryboard2 interface [Windows Animation],SetSkipDuration method, IUIAnimationStoryboard2.SetSkipDuration, IUIAnimationStoryboard2::SetSkipDuration, SetSkipDuration, SetSkipDuration method [Windows Animation], SetSkipDuration method [Windows Animation],IUIAnimationStoryboard2 interface, uianimation.iuianimationstoryboard2_setskipduration, uianimation/IUIAnimationStoryboard2::SetSkipDuration
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
-	IUIAnimationStoryboard2.SetSkipDuration
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboard2::SetSkipDuration


## -description


Specifies an offset from the beginning of a storyboard at which to start animating.


## -parameters




### -param secondsDuration [in]

The offset, or amount of time, to skip at the beginning of the storyboard.


## -returns



Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Calls to <b>SetSkipDuration</b> fail if the storyboard has been scheduled.

<b>SetSkipDuration</b> does not delay the start of a scheduled storyboard. See <a href="https://msdn.microsoft.com/D23F4833-413C-470B-8572-2DCB051576A3">IUIAnimationStoryboard2::SetLongestAcceptableDelay</a> for more info on how to set a delay for a scheduled storyboard.

This diagram shows a skip duration, or offset, for a storyboard. 

<img alt="Illustration of a storyboard offset" src="Images/SetSkipDuration.png"/>




## -see-also




<a href="https://msdn.microsoft.com/507B6C2B-92C6-4AEB-82D5-3F14A332D41F">IUIAnimationStoryboard2</a>



<a href="https://msdn.microsoft.com/D23F4833-413C-470B-8572-2DCB051576A3">SetLongestAcceptableDelay</a>
 

 

