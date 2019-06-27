---
UID: NF:uianimation.IUIAnimationManager2.Pause
title: IUIAnimationManager2::Pause (uianimation.h)
author: windows-sdk-content
description: Pauses all animations.
old-location: uianimation\iuianimationmanager2_pause.htm
tech.root: UIAnimation
ms.assetid: AA8EEFD5-A386-4DF1-BCBE-12A92D235E98
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],Pause method, IUIAnimationManager2.Pause, IUIAnimationManager2::Pause, Pause, Pause method [Windows Animation], Pause method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_pause, uianimation/IUIAnimationManager2::Pause
ms.topic: method
f1_keywords: 
 - "uianimation/IUIAnimationManager2.Pause"
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
ms.custom: 19H1
---

# IUIAnimationManager2::Pause


## -description


Pauses all animations.


## -parameters






## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



When an animation manager is paused, its status is set to <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/ne-uianimation-__midl___midl_itf_uianimation_0000_0000_0002">UI_ANIMATION_MANAGER_IDLE</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">IUIAnimationManager2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getstatus">IUIAnimationManager::GetStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-resume">IUIAnimationManager::Resume</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/ne-uianimation-__midl___midl_itf_uianimation_0000_0000_0002">UI_ANIMATION_MANAGER_STATUS</a>
 

 

