---
UID: NF:uianimation.IUIAnimationManager.CreateAnimationVariable
title: IUIAnimationManager::CreateAnimationVariable (uianimation.h)
description: Creates a new animation variable. (IUIAnimationManager.CreateAnimationVariable)
helpviewer_keywords: ["CreateAnimationVariable","CreateAnimationVariable method [Windows Animation]","CreateAnimationVariable method [Windows Animation]","IUIAnimationManager interface","IUIAnimationManager interface [Windows Animation]","CreateAnimationVariable method","IUIAnimationManager.CreateAnimationVariable","IUIAnimationManager::CreateAnimationVariable","uianimation.iuianimationmanager_createanimationvariable","uianimation/IUIAnimationManager::CreateAnimationVariable"]
old-location: uianimation\iuianimationmanager_createanimationvariable.htm
tech.root: UIAnimation
ms.assetid: e4c38e78-1b9e-4918-ba15-6a4c5c390c07
ms.date: 12/05/2018
ms.keywords: CreateAnimationVariable, CreateAnimationVariable method [Windows Animation], CreateAnimationVariable method [Windows Animation],IUIAnimationManager interface, IUIAnimationManager interface [Windows Animation],CreateAnimationVariable method, IUIAnimationManager.CreateAnimationVariable, IUIAnimationManager::CreateAnimationVariable, uianimation.iuianimationmanager_createanimationvariable, uianimation/IUIAnimationManager::CreateAnimationVariable
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
 - IUIAnimationManager::CreateAnimationVariable
 - uianimation/IUIAnimationManager::CreateAnimationVariable
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
 - IUIAnimationManager.CreateAnimationVariable
---

# IUIAnimationManager::CreateAnimationVariable


## -description

Creates a new animation variable.

## -parameters

### -param initialValue [in]

The initial value for the new animation variable.

### -param variable [out]

The new animation variable.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

The initial value of an animation variable is specified when the variable is created. After an animation variable is created, its value cannot be changed directly; it must be updated through the animation manager.

An animation variable is typically created to represent each visual characteristic that is to be animated. For example, an application might create two animation variables for the X and Y coordinates of an object that can move freely within a window.


#### Examples

For an example, see <a href="/windows/desktop/UIAnimation/create-animation-variables">Create Animation Variables</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager">IUIAnimationManager</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>
