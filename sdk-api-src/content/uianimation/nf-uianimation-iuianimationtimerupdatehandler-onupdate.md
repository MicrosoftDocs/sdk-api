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

# IUIAnimationTimerUpdateHandler::OnUpdate


## -description



      Handles update events from the timer.


## -parameters




### -param timeNow [in]


            The current timer time, in seconds.


### -param result [out]

 Receives a member of the <a href="https://msdn.microsoft.com/19b1d80f-39b3-4046-aa6a-5312e004b4b0">UI_ANIMATION_UPDATE_RESULT</a> enumeration, indicating whether any animation variables changed as a result of the update.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method is used by the <a href="https://msdn.microsoft.com/89e8f1be-fc4e-45e3-af7d-58556a114194">UIAnimationTimer</a> object to update the state of the <a href="https://msdn.microsoft.com/45c9c64b-9a06-4396-b715-d984655fe64c">UIAnimationManager</a> object. The <b>UIAnimationTimer</b> object calls <a href="https://msdn.microsoft.com/3a09537a-6cf7-4824-90c6-265dafa07a1b">UIAnimationTimerEventHandler::OnPostUpdate</a> only when calls to this method return a result of <b>UI_ANIMATION_UPDATE_VARIABLES_CHANGED</b>.




## -see-also




<a href="https://msdn.microsoft.com/3a09537a-6cf7-4824-90c6-265dafa07a1b">
      
      IUIAnimationTimerEventHandler::OnPostUpdate</a>



<a href="https://msdn.microsoft.com/4f3dcac0-c800-48e5-82d6-b6bc3fb0409b">
      IUIAnimationTimerEventHandler::OnPreUpdate</a>



<a href="https://msdn.microsoft.com/f155ed12-d493-48a0-9bdf-0e1e79cbcd38">IUIAnimationTimerUpdateHandler</a>
 

 

