---
UID: NF:uianimation.IUIAnimationTimerClientEventHandler.OnTimerClientStatusChanged
title: IUIAnimationTimerClientEventHandler::OnTimerClientStatusChanged
author: windows-sdk-content
description: Handles events that occur when the status of the timer's client changes.
old-location: uianimation\iuianimationtimerclienteventhandler_ontimerclientstatuschanged.htm
old-project: UIAnimation
ms.assetid: a2c161ce-937e-449a-884f-89a8a847d8aa
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUIAnimationTimerClientEventHandler interface [Windows Animation],OnTimerClientStatusChanged method, IUIAnimationTimerClientEventHandler.OnTimerClientStatusChanged, IUIAnimationTimerClientEventHandler::OnTimerClientStatusChanged, OnTimerClientStatusChanged, OnTimerClientStatusChanged method [Windows Animation], OnTimerClientStatusChanged method [Windows Animation],IUIAnimationTimerClientEventHandler interface, uianimation.iuianimationtimerclienteventhandler_ontimerclientstatuschanged, uianimation/IUIAnimationTimerClientEventHandler::OnTimerClientStatusChanged
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps \| UWP apps]
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
 - IUIAnimationTimerClientEventHandler.OnTimerClientStatusChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
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



<a href="https://msdn.microsoft.com/c7383df5-dbd4-4cae-a682-47f84c2e8106">IUIAnimationTimerUpdateHandler::ClearTimerClientEventHandler</a>



<a href="https://msdn.microsoft.com/ce213fc5-1329-413f-abf1-a4ab7c78818e">IUIAnimationTimerUpdateHandler::SetTimerClientEventHandler</a>



<a href="https://msdn.microsoft.com/45a445d1-cbe2-4588-a184-7d7bab6bc1ee">UI_ANIMATION_TIMER_CLIENT_STATUS</a>
 

 

