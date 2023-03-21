---
UID: NF:uianimation.IUIAnimationManager2.CreateAnimationVariable
title: IUIAnimationManager2::CreateAnimationVariable (uianimation.h)
description: Creates a new animation variable. (IUIAnimationManager2.CreateAnimationVariable)
helpviewer_keywords: ["CreateAnimationVariable","CreateAnimationVariable method [Windows Animation]","CreateAnimationVariable method [Windows Animation]","IUIAnimationManager2 interface","IUIAnimationManager2 interface [Windows Animation]","CreateAnimationVariable method","IUIAnimationManager2.CreateAnimationVariable","IUIAnimationManager2::CreateAnimationVariable","uianimation.iuianimationmanager2_createanimationvariable","uianimation/IUIAnimationManager2::CreateAnimationVariable"]
old-location: uianimation\iuianimationmanager2_createanimationvariable.htm
tech.root: UIAnimation
ms.assetid: 5E963D24-2436-4B8F-8806-69E521EC83AF
ms.date: 12/05/2018
ms.keywords: CreateAnimationVariable, CreateAnimationVariable method [Windows Animation], CreateAnimationVariable method [Windows Animation],IUIAnimationManager2 interface, IUIAnimationManager2 interface [Windows Animation],CreateAnimationVariable method, IUIAnimationManager2.CreateAnimationVariable, IUIAnimationManager2::CreateAnimationVariable, uianimation.iuianimationmanager2_createanimationvariable, uianimation/IUIAnimationManager2::CreateAnimationVariable
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
 - IUIAnimationManager2::CreateAnimationVariable
 - uianimation/IUIAnimationManager2::CreateAnimationVariable
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
 - IUIAnimationManager2.CreateAnimationVariable
---

# IUIAnimationManager2::CreateAnimationVariable


## -description

Creates a new animation variable.

## -parameters

### -param initialValue [in]

The initial value for the animation variable.

### -param variable [out, retval]

The new animation variable.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

The initial value of an animation variable is specified when the variable is created. After an animation variable is created, its value cannot be changed directly; it must be updated through the animation manager.

An animation variable is typically created to represent each visual characteristic that is to be animated. For example, an application might create two animation variables for the X and Y coordinates of an object that can move freely within a window.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">IUIAnimationManager2</a>
