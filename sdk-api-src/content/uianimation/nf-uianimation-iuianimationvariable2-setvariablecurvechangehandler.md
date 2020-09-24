---
UID: NF:uianimation.IUIAnimationVariable2.SetVariableCurveChangeHandler
title: IUIAnimationVariable2::SetVariableCurveChangeHandler (uianimation.h)
description: Specifies a handler for changes to the animation curve of the animation variable.
helpviewer_keywords: ["IUIAnimationVariable2 interface [Windows Animation]","SetVariableCurveChangeHandler method","IUIAnimationVariable2.SetVariableCurveChangeHandler","IUIAnimationVariable2::SetVariableCurveChangeHandler","SetVariableCurveChangeHandler","SetVariableCurveChangeHandler method [Windows Animation]","SetVariableCurveChangeHandler method [Windows Animation]","IUIAnimationVariable2 interface","uianimation.iuianimationvariable2_setvariablecurvechangehandler","uianimation/IUIAnimationVariable2::SetVariableCurveChangeHandler"]
old-location: uianimation\iuianimationvariable2_setvariablecurvechangehandler.htm
tech.root: UIAnimation
ms.assetid: 98C95C85-30C9-4E3E-82FE-E3D4C7ECAE0B
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariable2 interface [Windows Animation],SetVariableCurveChangeHandler method, IUIAnimationVariable2.SetVariableCurveChangeHandler, IUIAnimationVariable2::SetVariableCurveChangeHandler, SetVariableCurveChangeHandler, SetVariableCurveChangeHandler method [Windows Animation], SetVariableCurveChangeHandler method [Windows Animation],IUIAnimationVariable2 interface, uianimation.iuianimationvariable2_setvariablecurvechangehandler, uianimation/IUIAnimationVariable2::SetVariableCurveChangeHandler
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
 - IUIAnimationVariable2::SetVariableCurveChangeHandler
 - uianimation/IUIAnimationVariable2::SetVariableCurveChangeHandler
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
 - IUIAnimationVariable2.SetVariableCurveChangeHandler
---

# IUIAnimationVariable2::SetVariableCurveChangeHandler


## -description

Specifies a handler for changes to the animation curve of the animation variable.

## -parameters

### -param handler [in, optional]

A pointer to the handler for changes to the animation curve of the animation variable. This parameter can be <b>NULL</b>.

## -returns

Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariablecurvechangehandler2">IUIAnimationVariableCurveChangeHandler2</a>