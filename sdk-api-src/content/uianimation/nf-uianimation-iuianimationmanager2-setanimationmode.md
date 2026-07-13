---
UID: NF:uianimation.IUIAnimationManager2.SetAnimationMode
title: IUIAnimationManager2::SetAnimationMode (uianimation.h)
description: Sets the animation mode. (IUIAnimationManager2.SetAnimationMode)
helpviewer_keywords: ["IUIAnimationManager2 interface [Windows Animation]","SetAnimationMode method","IUIAnimationManager2.SetAnimationMode","IUIAnimationManager2::SetAnimationMode","SetAnimationMode","SetAnimationMode method [Windows Animation]","SetAnimationMode method [Windows Animation]","IUIAnimationManager2 interface","uianimation.iuianimationmanager2_setanimationmode","uianimation/IUIAnimationManager2::SetAnimationMode"]
old-location: uianimation\iuianimationmanager2_setanimationmode.htm
tech.root: UIAnimation
ms.assetid: BA568B62-7A85-4758-BB04-B4AF617A8443
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],SetAnimationMode method, IUIAnimationManager2.SetAnimationMode, IUIAnimationManager2::SetAnimationMode, SetAnimationMode, SetAnimationMode method [Windows Animation], SetAnimationMode method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_setanimationmode, uianimation/IUIAnimationManager2::SetAnimationMode
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
 - IUIAnimationManager2::SetAnimationMode
 - uianimation/IUIAnimationManager2::SetAnimationMode
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
 - IUIAnimationManager2.SetAnimationMode
---

# IUIAnimationManager2::SetAnimationMode


## -description

Sets the animation mode.

## -parameters

### -param mode [in]

The animation mode.

## -returns

Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Use this method to enable or disable animation globally. While animation is disabled, all storyboards finish immediately when they are scheduled. The default mode is <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_mode">UI_ANIMATION_MODE_SYSTEM_DEFAULT</a>, which lets Windows decide when to enable or disable animation in the application.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">IUIAnimationManager2</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_mode">UI_ANIMATION_MODE</a>
