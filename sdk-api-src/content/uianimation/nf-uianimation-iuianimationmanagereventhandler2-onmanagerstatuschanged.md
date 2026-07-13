---
UID: NF:uianimation.IUIAnimationManagerEventHandler2.OnManagerStatusChanged
title: IUIAnimationManagerEventHandler2::OnManagerStatusChanged (uianimation.h)
description: Handles status changes to an animation manager. (IUIAnimationManagerEventHandler2.OnManagerStatusChanged)
helpviewer_keywords: ["IUIAnimationManagerEventHandler2 interface [Windows Animation]","OnManagerStatusChanged method","IUIAnimationManagerEventHandler2.OnManagerStatusChanged","IUIAnimationManagerEventHandler2::OnManagerStatusChanged","OnManagerStatusChanged","OnManagerStatusChanged method [Windows Animation]","OnManagerStatusChanged method [Windows Animation]","IUIAnimationManagerEventHandler2 interface","uianimation.iuianimationmanagereventhandler2_onmanagerstatuschanged","uianimation/IUIAnimationManagerEventHandler2::OnManagerStatusChanged"]
old-location: uianimation\iuianimationmanagereventhandler2_onmanagerstatuschanged.htm
tech.root: UIAnimation
ms.assetid: 398A52B3-E7FA-466E-BCED-0A6E91633CF7
ms.date: 12/05/2018
ms.keywords: IUIAnimationManagerEventHandler2 interface [Windows Animation],OnManagerStatusChanged method, IUIAnimationManagerEventHandler2.OnManagerStatusChanged, IUIAnimationManagerEventHandler2::OnManagerStatusChanged, OnManagerStatusChanged, OnManagerStatusChanged method [Windows Animation], OnManagerStatusChanged method [Windows Animation],IUIAnimationManagerEventHandler2 interface, uianimation.iuianimationmanagereventhandler2_onmanagerstatuschanged, uianimation/IUIAnimationManagerEventHandler2::OnManagerStatusChanged
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
 - IUIAnimationManagerEventHandler2::OnManagerStatusChanged
 - uianimation/IUIAnimationManagerEventHandler2::OnManagerStatusChanged
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
 - IUIAnimationManagerEventHandler2.OnManagerStatusChanged
---

# IUIAnimationManagerEventHandler2::OnManagerStatusChanged


## -description

Handles status changes to an <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">animation manager</a>.

## -parameters

### -param newStatus [in]

The new status of the animation manager.

### -param previousStatus [in]

The previous status of the animation manager.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Calls made to other Windows Animation methods from <b>IUIAnimationManager2::OnManagerStatusChanged</b> fail and return <b>UI_E_ILLEGAL_REENTRANCY</b>.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-getstatus">IUIAnimationManager2::GetStatus</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanagereventhandler2">IUIAnimationManagerEventHandler2</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_manager_status">UI_ANIMATION_MANAGER_STATUS</a>
