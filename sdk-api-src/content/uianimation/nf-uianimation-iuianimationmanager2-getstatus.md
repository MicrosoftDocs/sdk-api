---
UID: NF:uianimation.IUIAnimationManager2.GetStatus
title: IUIAnimationManager2::GetStatus (uianimation.h)
description: Gets the status of the animation manager. (IUIAnimationManager2.GetStatus)
helpviewer_keywords: ["GetStatus","GetStatus method [Windows Animation]","GetStatus method [Windows Animation]","IUIAnimationManager2 interface","IUIAnimationManager2 interface [Windows Animation]","GetStatus method","IUIAnimationManager2.GetStatus","IUIAnimationManager2::GetStatus","uianimation.iuianimationmanager2_getstatus","uianimation/IUIAnimationManager2::GetStatus"]
old-location: uianimation\iuianimationmanager2_getstatus.htm
tech.root: UIAnimation
ms.assetid: E989CED1-C6B7-4086-944E-924836AA7ECB
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Windows Animation], GetStatus method [Windows Animation],IUIAnimationManager2 interface, IUIAnimationManager2 interface [Windows Animation],GetStatus method, IUIAnimationManager2.GetStatus, IUIAnimationManager2::GetStatus, uianimation.iuianimationmanager2_getstatus, uianimation/IUIAnimationManager2::GetStatus
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAnimationManager2::GetStatus
 - uianimation/IUIAnimationManager2::GetStatus
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
 - IUIAnimationManager2.GetStatus
---

# IUIAnimationManager2::GetStatus


## -description

Gets the status of the animation manager.

## -parameters

### -param status [out]

The status of the animation manager.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">IUIAnimationManager2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanagereventhandler-onmanagerstatuschanged">IUIAnimationManagerEventHandler::OnManagerStatusChanged</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_manager_status">UI_ANIMATION_MANAGER_STATUS</a>
