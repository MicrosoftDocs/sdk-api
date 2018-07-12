---
UID: NF:uianimation.IUIAnimationManager2.SetDefaultLongestAcceptableDelay
title: IUIAnimationManager2::SetDefaultLongestAcceptableDelay
author: windows-sdk-content
description: Sets the default acceptable animation delay. This is the length of time that may pass before storyboards begin.
old-location: uianimation\iuianimationmanager2_setdefaultlongestacceptabledelay.htm
old-project: UIAnimation
ms.assetid: CB00C22B-9837-43AD-9E04-30182B7386E9
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],SetDefaultLongestAcceptableDelay method, IUIAnimationManager2.SetDefaultLongestAcceptableDelay, IUIAnimationManager2::SetDefaultLongestAcceptableDelay, SetDefaultLongestAcceptableDelay, SetDefaultLongestAcceptableDelay method [Windows Animation], SetDefaultLongestAcceptableDelay method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_setdefaultlongestacceptabledelay, uianimation/IUIAnimationManager2::SetDefaultLongestAcceptableDelay
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
 - IUIAnimationManager2.SetDefaultLongestAcceptableDelay
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationManager2::SetDefaultLongestAcceptableDelay


## -description



      Sets the default acceptable animation delay. This is the length of time that may pass before storyboards begin.


## -parameters




### -param delay [in]


                The default delay. This parameter can be a positive value, or <a href="https://msdn.microsoft.com/9971A612-69D7-49AB-8865-B8F29C4CD4C8">UI_ANIMATION_SECONDS_EVENTUALLY</a> (-1) to indicate that any finite delay is acceptable.


## -returns



Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



For Windows Animation to schedule a storyboard successfully, the storyboard must begin before the longest acceptable delay has elapsed. Windows Animation determines this delay in the following order: the delay value set by calling <a href="https://msdn.microsoft.com/5f87a4b1-8db9-42ba-963f-664db588c520">IUIAnimationStoryboard::SetLongestAcceptableDelay</a> for this specific storyboard, the delay value set by calling this method, or 0.0 if neither method has been called.




## -see-also




<a href="https://msdn.microsoft.com/BD7DAD23-2A7D-4EE7-9BCF-8380F928674D">IUIAnimationManager2</a>



<a href="https://msdn.microsoft.com/5f87a4b1-8db9-42ba-963f-664db588c520">
      IUIAnimationStoryboard::SetLongestAcceptableDelay</a>
 

 

