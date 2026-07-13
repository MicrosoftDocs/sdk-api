---
UID: NF:uianimation.IUIAnimationManager.GetStatus
title: IUIAnimationManager::GetStatus (uianimation.h)
description: Gets the status of the animation manager. (IUIAnimationManager.GetStatus)
helpviewer_keywords: ["GetStatus","GetStatus method [Windows Animation]","GetStatus method [Windows Animation]","IUIAnimationManager interface","IUIAnimationManager interface [Windows Animation]","GetStatus method","IUIAnimationManager.GetStatus","IUIAnimationManager::GetStatus","uianimation.iuianimationmanager_getstatus","uianimation/IUIAnimationManager::GetStatus"]
old-location: uianimation\iuianimationmanager_getstatus.htm
tech.root: UIAnimation
ms.assetid: 838140c3-12ca-4909-a0f8-713b5472e5a9
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Windows Animation], GetStatus method [Windows Animation],IUIAnimationManager interface, IUIAnimationManager interface [Windows Animation],GetStatus method, IUIAnimationManager.GetStatus, IUIAnimationManager::GetStatus, uianimation.iuianimationmanager_getstatus, uianimation/IUIAnimationManager::GetStatus
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAnimationManager::GetStatus
 - uianimation/IUIAnimationManager::GetStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationManager.GetStatus
---

# IUIAnimationManager::GetStatus


## -description

Gets the status of the animation manager.

## -parameters

### -param status [out]

The status.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanagereventhandler-onmanagerstatuschanged">IUIAnimationManagerEventHandler::OnManagerStatusChanged</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_manager_status">UI_ANIMATION_MANAGER_STATUS</a>
