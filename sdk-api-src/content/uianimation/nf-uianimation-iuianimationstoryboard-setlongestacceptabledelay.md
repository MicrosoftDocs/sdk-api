---
UID: NF:uianimation.IUIAnimationStoryboard.SetLongestAcceptableDelay
title: IUIAnimationStoryboard::SetLongestAcceptableDelay
author: windows-driver-content
description: Sets the longest acceptable delay before the scheduled storyboard begins.
old-location: uianimation\iuianimationstoryboard_setlongestacceptabledelay.htm
old-project: UIAnimation
ms.assetid: 5f87a4b1-8db9-42ba-963f-664db588c520
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IUIAnimationStoryboard interface [Windows Animation],SetLongestAcceptableDelay method, IUIAnimationStoryboard.SetLongestAcceptableDelay, IUIAnimationStoryboard::SetLongestAcceptableDelay, SetLongestAcceptableDelay, SetLongestAcceptableDelay method [Windows Animation], SetLongestAcceptableDelay method [Windows Animation],IUIAnimationStoryboard interface, uianimation.iuianimationstoryboard_setlongestacceptabledelay, uianimation/IUIAnimationStoryboard::SetLongestAcceptableDelay
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IUIAnimationStoryboard.SetLongestAcceptableDelay
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationStoryboard::SetLongestAcceptableDelay


## -description



      Sets the longest acceptable delay before the scheduled storyboard begins.


## -parameters




### -param delay [in]


               The longest acceptable delay. This parameter can be a positive value, or <b>UI_ANIMATION_SECONDS_EVENTUALLY</b> (-1) to indicate that any finite delay is acceptable.


## -returns




            If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.            
            




## -remarks



For a storyboard to be successfully scheduled, it must begin before the longest acceptable delay has elapsed. This delay is determined in the following order: the delay value set by calling this method, the delay value set by calling the <a href="https://msdn.microsoft.com/27182009-1614-41a0-9b55-7c1dcb494883">IUIAnimationManager::SetDefaultLongestAcceptableDelay</a> method, or 0.0 if neither of these methods has been called.




## -see-also




<a href="https://msdn.microsoft.com/27182009-1614-41a0-9b55-7c1dcb494883">
      IUIAnimationManager::SetDefaultLongestAcceptableDelay</a>



<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>
 

 

