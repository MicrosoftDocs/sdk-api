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

# IUIAnimationTimerClientEventHandler::OnTimerClientStatusChanged


## -description



      Handles events that occur when the status of the timer's  client changes.


## -parameters




### -param newStatus [in]

The new status of the timer's client.


### -param previousStatus [in]


               The previous status of the timer's client.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/8ca8f7d8-e698-4c55-8241-5c8f7b47f0e8">IUIAnimationTimerClientEventHandler</a>



<a href="https://msdn.microsoft.com/c7383df5-dbd4-4cae-a682-47f84c2e8106">
      IUIAnimationTimerUpdateHandler::ClearTimerClientEventHandler</a>



<a href="https://msdn.microsoft.com/ce213fc5-1329-413f-abf1-a4ab7c78818e">
      IUIAnimationTimerUpdateHandler::SetTimerClientEventHandler</a>



<a href="https://msdn.microsoft.com/45a445d1-cbe2-4588-a184-7d7bab6bc1ee">UI_ANIMATION_TIMER_CLIENT_STATUS</a>
 

 

