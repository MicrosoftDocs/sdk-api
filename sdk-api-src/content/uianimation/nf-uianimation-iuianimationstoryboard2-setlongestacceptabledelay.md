---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

