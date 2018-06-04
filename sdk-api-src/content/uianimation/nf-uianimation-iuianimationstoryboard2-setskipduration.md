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
 

 

