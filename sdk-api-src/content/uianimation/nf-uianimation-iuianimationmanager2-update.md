---
UID: NF:uianimation.IUIAnimationManager2.Update
title: IUIAnimationManager2::Update (uianimation.h)
description: Updates the values of all animation variables. (IUIAnimationManager2.Update)
helpviewer_keywords: ["IUIAnimationManager2 interface [Windows Animation]","Update method","IUIAnimationManager2.Update","IUIAnimationManager2::Update","Update","Update method [Windows Animation]","Update method [Windows Animation]","IUIAnimationManager2 interface","uianimation.iuianimationmanager2_update","uianimation/IUIAnimationManager2::Update"]
old-location: uianimation\iuianimationmanager2_update.htm
tech.root: UIAnimation
ms.assetid: 5735ABDB-E1AE-41C0-9F37-92084CEF6FAD
ms.date: 12/05/2018
ms.keywords: IUIAnimationManager2 interface [Windows Animation],Update method, IUIAnimationManager2.Update, IUIAnimationManager2::Update, Update, Update method [Windows Animation], Update method [Windows Animation],IUIAnimationManager2 interface, uianimation.iuianimationmanager2_update, uianimation/IUIAnimationManager2::Update
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
 - IUIAnimationManager2::Update
 - uianimation/IUIAnimationManager2::Update
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
 - IUIAnimationManager2.Update
---

# IUIAnimationManager2::Update


## -description

Updates the values of all animation variables.

## -parameters

### -param timeNow [in]

The current system time. This parameter must be greater than or equal to 0.0.

### -param updateResult [out, optional]

The result of the update.
            You can omit this parameter from calls to this method.

## -returns

Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Calling this method advances the animation manager to <i>timeNow</i>, changes the status of all storyboards as necessary, and updates any animation variables to appropriate interpolated values. If the animation manager is paused, no storyboards or variables are updated. If the animation  mode is <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_mode">UI_ANIMATION_MODE_DISABLED</a>, all scheduled storyboards finish playing immediately. If the values of any variables change during this call, the value of <i>updateResult</i> is <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_update_result">UI_ANIMATION_UPDATE_VARIABLES_CHANGED</a>; otherwise, it is <a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_update_result">UI_ANIMATION_UPDATE_NO_CHANGE</a>.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">IUIAnimationManager2</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-pause">IUIAnimationManager2::Pause</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-resume">IUIAnimationManager2::Resume</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager2-setanimationmode">IUIAnimationManager::SetAnimationMode</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_mode">UI_ANIMATION_MODE</a>



<a href="/windows/win32/api/uianimation/ne-uianimation-ui_animation_update_result">UI_ANIMATION_UPDATE_RESULT</a>
