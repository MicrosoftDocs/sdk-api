---
UID: NF:uianimation.IUIAnimationManager2.Pause
title: IUIAnimationManager2::Pause
author: windows-sdk-content
description: Pauses all animations.
old-location: uianimation\iuianimationmanager2_pause.htm
tech.root: UIAnimation
ms.assetid: AA8EEFD5-A386-4DF1-BCBE-12A92D235E98
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],Pause method, IUIAnimationManager2.Pause, IUIAnimationManager2::Pause, Pause, Pause method [Windows Animation], Pause method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_pause, uianimation/IUIAnimationManager2::Pause
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8, Windows 7 and Platform Update for Windows 7 [desktop apps \| UWP apps]
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
 - IUIAnimationManager2.Pause
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationManager2::Pause


## -description


Pauses all animations.


## -parameters






## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



When an animation manager is paused, its status is set to <a href="https://msdn.microsoft.com/499c74c0-d1e7-4ab4-9c3a-19c2e1abeda8">UI_ANIMATION_MANAGER_IDLE</a>.




## -see-also




<a href="https://msdn.microsoft.com/21f16c65-90aa-4b1f-93bc-8ee0488c6ded">IUIAnimationManager</a>



<a href="https://msdn.microsoft.com/BD7DAD23-2A7D-4EE7-9BCF-8380F928674D">IUIAnimationManager2</a>



<a href="https://msdn.microsoft.com/838140c3-12ca-4909-a0f8-713b5472e5a9">IUIAnimationManager::GetStatus</a>



<a href="https://msdn.microsoft.com/f29a9337-0ed0-46f8-ab77-8f82ab39d8df">IUIAnimationManager::Resume</a>



<a href="https://msdn.microsoft.com/499c74c0-d1e7-4ab4-9c3a-19c2e1abeda8">UI_ANIMATION_MANAGER_STATUS</a>
 

 

