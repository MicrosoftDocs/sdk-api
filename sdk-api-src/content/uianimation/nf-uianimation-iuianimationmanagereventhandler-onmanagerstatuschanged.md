---
UID: NF:uianimation.IUIAnimationManagerEventHandler.OnManagerStatusChanged
title: IUIAnimationManagerEventHandler::OnManagerStatusChanged (uianimation.h)
description: Handles status changes to an animation manager. (IUIAnimationManagerEventHandler.OnManagerStatusChanged)
helpviewer_keywords: ["IUIAnimationManagerEventHandler interface [Windows Animation]","OnManagerStatusChanged method","IUIAnimationManagerEventHandler.OnManagerStatusChanged","IUIAnimationManagerEventHandler::OnManagerStatusChanged","OnManagerStatusChanged","OnManagerStatusChanged method [Windows Animation]","OnManagerStatusChanged method [Windows Animation]","IUIAnimationManagerEventHandler interface","uianimation.iuianimationmanagereventhandler_onmanagerstatuschanged","uianimation/IUIAnimationManagerEventHandler::OnManagerStatusChanged"]
old-location: uianimation\iuianimationmanagereventhandler_onmanagerstatuschanged.htm
tech.root: UIAnimation
ms.assetid: 17f98ff5-f18e-44be-a8bd-bc5a6467fa83
ms.date: 12/05/2018
ms.keywords: IUIAnimationManagerEventHandler interface [Windows Animation],OnManagerStatusChanged method, IUIAnimationManagerEventHandler.OnManagerStatusChanged, IUIAnimationManagerEventHandler::OnManagerStatusChanged, OnManagerStatusChanged, OnManagerStatusChanged method [Windows Animation], OnManagerStatusChanged method [Windows Animation],IUIAnimationManagerEventHandler interface, uianimation.iuianimationmanagereventhandler_onmanagerstatuschanged, uianimation/IUIAnimationManagerEventHandler::OnManagerStatusChanged
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
 - IUIAnimationManagerEventHandler::OnManagerStatusChanged
 - uianimation/IUIAnimationManagerEventHandler::OnManagerStatusChanged
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
 - IUIAnimationManagerEventHandler.OnManagerStatusChanged
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

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

A call made in this callback method to any other animation method results in the call failing and returning <b>UI_E_ILLEGAL_REENTRANCY</b>.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-getstatus">IUIAnimationManager::GetStatus</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanagereventhandler">IUIAnimationManagerEventHandler</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_manager_status">UI_ANIMATION_MANAGER_STATUS</a>
