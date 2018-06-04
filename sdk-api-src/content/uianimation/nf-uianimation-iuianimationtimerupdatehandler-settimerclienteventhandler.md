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

# IUIAnimationTimerUpdateHandler::SetTimerClientEventHandler


## -description



      Specifies a handler for timer client status change events.


## -parameters




### -param handler [in]


               A handler for timer client events.  The specified object must implement
               <a href="https://msdn.microsoft.com/8ca8f7d8-e698-4c55-8241-5c8f7b47f0e8">IUIAnimationTimerUpdateHandler</a>.
            


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



If the update handler is already connected to the timer, this method returns <b>UI_E_TIMER_CLIENT_ALREADY_CONNECTED.</b>




## -see-also




<a href="https://msdn.microsoft.com/f155ed12-d493-48a0-9bdf-0e1e79cbcd38">IUIAnimationTimerUpdateHandler</a>



<a href="https://msdn.microsoft.com/c7383df5-dbd4-4cae-a682-47f84c2e8106">
      IUIAnimationTimerUpdateHandler::ClearTimerClientEventHandler</a>
 

 

