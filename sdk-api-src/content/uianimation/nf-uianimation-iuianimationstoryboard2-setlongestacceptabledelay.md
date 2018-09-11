---
UID: NF:uianimation.IUIAnimationStoryboard2.SetLongestAcceptableDelay
title: IUIAnimationStoryboard2::SetLongestAcceptableDelay
author: windows-sdk-content
description: Sets the longest acceptable delay before the scheduled storyboard begins.
old-location: uianimation\iuianimationstoryboard2_setlongestacceptabledelay.htm
tech.root: UIAnimation
ms.assetid: D23F4833-413C-470B-8572-2DCB051576A3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUIAnimationStoryboard2 interface [Windows Animation],SetLongestAcceptableDelay method, IUIAnimationStoryboard2.SetLongestAcceptableDelay, IUIAnimationStoryboard2::SetLongestAcceptableDelay, SetLongestAcceptableDelay, SetLongestAcceptableDelay method [Windows Animation], SetLongestAcceptableDelay method [Windows Animation],IUIAnimationStoryboard2 interface, uianimation.iuianimationstoryboard2_setlongestacceptabledelay, uianimation/IUIAnimationStoryboard2::SetLongestAcceptableDelay
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps \| UWP apps]
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
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationStoryboard2.SetLongestAcceptableDelay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationStoryboard2::SetLongestAcceptableDelay


## -description


Sets the longest acceptable delay before the scheduled storyboard begins.


## -parameters




### -param delay [in]

The longest acceptable delay. This parameter can be a positive value, or <a href="https://msdn.microsoft.com/9971A612-69D7-49AB-8865-B8F29C4CD4C8">UI_ANIMATION_SECONDS_EVENTUALLY</a> (-1) to indicate that any finite delay is acceptable.


## -returns



Returns <b>S_OK</b> if successful; otherwise an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



For Windows Animation to schedule a storyboard successfully, the storyboard must begin before the longest acceptable delay has elapsed. Windows Animation determines this delay in the following order: the delay value set by calling this method, the delay value set by calling the <a href="https://msdn.microsoft.com/CB00C22B-9837-43AD-9E04-30182B7386E9">IUIAnimationManager2::SetDefaultLongestAcceptableDelay</a> method, or 0.0 if neither of these methods has been called.

 Use <a href="https://msdn.microsoft.com/177623D7-5516-41EA-9014-61B150E527D9">IUIAnimationStoryboard2::SetSkipDuration</a> to start a storyboard animation at a specified offset instead of delaying the start of a storyboard.




## -see-also




<a href="https://msdn.microsoft.com/507B6C2B-92C6-4AEB-82D5-3F14A332D41F">IUIAnimationStoryboard2</a>



<a href="https://msdn.microsoft.com/177623D7-5516-41EA-9014-61B150E527D9">SetSkipDuration</a>
 

 

