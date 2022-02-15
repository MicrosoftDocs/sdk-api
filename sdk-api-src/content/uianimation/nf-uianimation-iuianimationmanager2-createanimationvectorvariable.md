---
UID: NF:uianimation.IUIAnimationManager2.CreateAnimationVectorVariable
title: IUIAnimationManager2::CreateAnimationVectorVariable (uianimation.h)
description: Creates a new animation variable for each specified dimension.
helpviewer_keywords: ["CreateAnimationVectorVariable","CreateAnimationVectorVariable method [Windows Animation]","CreateAnimationVectorVariable method [Windows Animation]","IUIAnimationManager2 interface","IUIAnimationManager2 interface [Windows Animation]","CreateAnimationVectorVariable method","IUIAnimationManager2.CreateAnimationVectorVariable","IUIAnimationManager2::CreateAnimationVectorVariable","uianimation.iuianimationmanager2_createanimationvectorvariable","uianimation/IUIAnimationManager2::CreateAnimationVectorVariable"]
old-location: uianimation\iuianimationmanager2_createanimationvectorvariable.htm
tech.root: UIAnimation
ms.assetid: b102f7d7-1a0b-40b5-bcc6-fa82dbcb4156
ms.date: 12/05/2018
ms.keywords: CreateAnimationVectorVariable, CreateAnimationVectorVariable method [Windows Animation], CreateAnimationVectorVariable method [Windows Animation],IUIAnimationManager2 interface, IUIAnimationManager2 interface [Windows Animation],CreateAnimationVectorVariable method, IUIAnimationManager2.CreateAnimationVectorVariable, IUIAnimationManager2::CreateAnimationVectorVariable, uianimation.iuianimationmanager2_createanimationvectorvariable, uianimation/IUIAnimationManager2::CreateAnimationVectorVariable
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
 - IUIAnimationManager2::CreateAnimationVectorVariable
 - uianimation/IUIAnimationManager2::CreateAnimationVectorVariable
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
 - IUIAnimationManager2.CreateAnimationVectorVariable
---

# IUIAnimationManager2::CreateAnimationVectorVariable


## -description

Creates a new animation variable for each specified dimension.

## -parameters

### -param initialValue [in]

A vector (of size <i>cDimension</i>) of  initial values for the animation variable.

### -param cDimension [in]

The number of dimensions that require animated values. This parameter specifies the number of values listed in <i>initialValue</i>.

### -param variable [out, retval]

The new animation variable.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

The initial value of an animation variable is specified when the variable is created. After an animation variable is created, its value cannot be changed directly; it must be updated through the animation manager.

An animation variable is typically created to represent each visual characteristic that is to be animated. For example, an application might create three animation variables for the X, Y, and Z coordinates of an object that can move freely within a three-dimensional space.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationmanager2">IUIAnimationManager2</a>