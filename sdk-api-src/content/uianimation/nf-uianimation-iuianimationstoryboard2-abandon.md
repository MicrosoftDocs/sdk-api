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
 

 

