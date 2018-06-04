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

# IUIAnimationStoryboard::Finish


## -description


Finishes the storyboard within the specified time, compressing the storyboard if necessary.


## -parameters




### -param completionDeadline [in]


                The maximum amount of time that the storyboard can use to finish playing.


## -returns




            If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method has no effect on storyboard events. Events continue to be raised as expected while the storyboard plays.




## -see-also




<a href="https://msdn.microsoft.com/db5ba70c-3904-4053-881a-b1412beb35f3">
      IUIAnimationManager::FinishAllStoryboards</a>



<a href="https://msdn.microsoft.com/6b30b660-dfa4-410f-a8de-58ea5c9a104d">IUIAnimationStoryboard</a>



<a href="https://msdn.microsoft.com/2350dbd0-3a67-4832-94dd-56adce80a387">
      IUIAnimationStoryboard::Abandon</a>



<a href="https://msdn.microsoft.com/82f915df-c031-41e9-8347-044b37793182">
      IUIAnimationStoryboard::Conclude</a>



<a href="https://msdn.microsoft.com/b47d4ffd-ae51-40e7-8f91-9d7b7b2901c8">
      IUIAnimationStoryboard::Schedule</a>
 

 

