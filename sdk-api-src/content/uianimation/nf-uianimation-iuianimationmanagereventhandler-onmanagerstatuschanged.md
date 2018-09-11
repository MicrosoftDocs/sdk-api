---
UID: NF:uianimation.IUIAnimationManagerEventHandler.OnManagerStatusChanged
title: IUIAnimationManagerEventHandler::OnManagerStatusChanged
author: windows-sdk-content
description: Handles status changes to an animation manager.
old-location: uianimation\iuianimationmanagereventhandler_onmanagerstatuschanged.htm
tech.root: UIAnimation
ms.assetid: 17f98ff5-f18e-44be-a8bd-bc5a6467fa83
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUIAnimationManagerEventHandler interface [Windows Animation],OnManagerStatusChanged method, IUIAnimationManagerEventHandler.OnManagerStatusChanged, IUIAnimationManagerEventHandler::OnManagerStatusChanged, OnManagerStatusChanged, OnManagerStatusChanged method [Windows Animation], OnManagerStatusChanged method [Windows Animation],IUIAnimationManagerEventHandler interface, uianimation.iuianimationmanagereventhandler_onmanagerstatuschanged, uianimation/IUIAnimationManagerEventHandler::OnManagerStatusChanged
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uianimation.h
req.include-header: 
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
 - IUIAnimationManagerEventHandler.OnManagerStatusChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationManagerEventHandler::OnManagerStatusChanged


## -description


Handles status changes to an animation manager.


## -parameters




### -param newStatus [in]

The new status.


### -param previousStatus [in]

The previous status.


## -returns



If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



A call made in this callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>.




## -see-also




<a href="https://msdn.microsoft.com/838140c3-12ca-4909-a0f8-713b5472e5a9">IUIAnimationManager::GetStatus</a>



<a href="https://msdn.microsoft.com/caefafb8-55f8-47c3-adc7-26708b90d2cd">IUIAnimationManagerEventHandler</a>



<a href="https://msdn.microsoft.com/499c74c0-d1e7-4ab4-9c3a-19c2e1abeda8">UI_ANIMATION_MANAGER_STATUS</a>
 

 

