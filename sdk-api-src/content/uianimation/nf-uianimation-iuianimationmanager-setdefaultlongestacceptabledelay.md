---
UID: NF:uianimation.IUIAnimationManager.SetDefaultLongestAcceptableDelay
title: IUIAnimationManager::SetDefaultLongestAcceptableDelay
author: windows-sdk-content
description: Sets the default acceptable animation delay. This is the length of time that may pass before storyboards begin.
old-location: uianimation\iuianimationmanager_setdefaultlongestacceptabledelay.htm
old-project: UIAnimation
ms.assetid: 27182009-1614-41a0-9b55-7c1dcb494883
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IUIAnimationManager interface [Windows Animation],SetDefaultLongestAcceptableDelay method, IUIAnimationManager.SetDefaultLongestAcceptableDelay, IUIAnimationManager::SetDefaultLongestAcceptableDelay, SetDefaultLongestAcceptableDelay, SetDefaultLongestAcceptableDelay method [Windows Animation], SetDefaultLongestAcceptableDelay method [Windows Animation],IUIAnimationManager interface, uianimation.iuianimationmanager_setdefaultlongestacceptabledelay, uianimation/IUIAnimationManager::SetDefaultLongestAcceptableDelay
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
-	IUIAnimationManager.SetDefaultLongestAcceptableDelay
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationManager::SetDefaultLongestAcceptableDelay


## -description



      Sets the default acceptable animation delay. This is the length of time that may pass before storyboards begin.


## -parameters




### -param delay [in]


                The default delay. This parameter can be a positive value, or <b>UI_ANIMATION_SECONDS_EVENTUALLY</b> (-1) to indicate that any finite delay is acceptable.


## -returns




            If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.            
            See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



For a storyboard to be successfully scheduled, it must begin before the longest acceptable delay has elapsed. This delay is determined in the following order: the delay value set by calling <a href="https://msdn.microsoft.com/5f87a4b1-8db9-42ba-963f-664db588c520">IUIAnimationStoryboard::SetLongestAcceptableDelay</a> for this specific storyboard, the delay value set by calling this method, or 0.0 if neither method has been called.




## -see-also




<a href="https://msdn.microsoft.com/21f16c65-90aa-4b1f-93bc-8ee0488c6ded">IUIAnimationManager</a>



<a href="https://msdn.microsoft.com/5f87a4b1-8db9-42ba-963f-664db588c520">
      IUIAnimationStoryboard::SetLongestAcceptableDelay</a>
 

 

