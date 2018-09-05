---
UID: NF:uianimation.IUIAnimationManager.Shutdown
title: IUIAnimationManager::Shutdown
author: windows-sdk-content
description: Shuts down the animation manager and all its associated objects.
old-location: uianimation\iuianimationmanager_shutdown.htm
old-project: UIAnimation
ms.assetid: 3bcce52c-d29a-423c-ae76-eb88cbe8c8df
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUIAnimationManager interface [Windows Animation],Shutdown method, IUIAnimationManager.Shutdown, IUIAnimationManager::Shutdown, Shutdown, Shutdown method [Windows Animation], Shutdown method [Windows Animation],IUIAnimationManager interface, uianimation.iuianimationmanager_shutdown, uianimation/IUIAnimationManager::Shutdown
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
 - IUIAnimationManager.Shutdown
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAnimation.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAnimationManager::Shutdown


## -description


Shuts down the animation manager and all its associated objects.


## -parameters






## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



Calling this method directs the animation manager, and all the objects it created, to 
         release all their pointers to other objects. After <b>IUIAnimationManager::Shutdown</b> has been called, no other methods may be called on the animation manager or any objects that it created. An application can call this method to clean up if there is any possibility that the application has introduced a reference cycle that includes some animation objects.




## -see-also




<a href="https://msdn.microsoft.com/21f16c65-90aa-4b1f-93bc-8ee0488c6ded">IUIAnimationManager</a>
 

 

