---
UID: NF:uianimation.IUIAnimationVariableCurveChangeHandler2.OnCurveChanged
title: IUIAnimationVariableCurveChangeHandler2::OnCurveChanged (uianimation.h)
description: Handles events that occur when the animation curve of an animation variable changes.
helpviewer_keywords: ["IUIAnimationVariableCurveChangeHandler2 interface [Windows Animation]","OnCurveChanged method","IUIAnimationVariableCurveChangeHandler2.OnCurveChanged","IUIAnimationVariableCurveChangeHandler2::OnCurveChanged","OnCurveChanged","OnCurveChanged method [Windows Animation]","OnCurveChanged method [Windows Animation]","IUIAnimationVariableCurveChangeHandler2 interface","uianimation.iuianimationvariablecurvechangehandler2_oncurvechanged","uianimation/IUIAnimationVariableCurveChangeHandler2::OnCurveChanged"]
old-location: uianimation\iuianimationvariablecurvechangehandler2_oncurvechanged.htm
tech.root: UIAnimation
ms.assetid: CD0F59F7-9383-4602-8A97-356AEAB0FD82
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariableCurveChangeHandler2 interface [Windows Animation],OnCurveChanged method, IUIAnimationVariableCurveChangeHandler2.OnCurveChanged, IUIAnimationVariableCurveChangeHandler2::OnCurveChanged, OnCurveChanged, OnCurveChanged method [Windows Animation], OnCurveChanged method [Windows Animation],IUIAnimationVariableCurveChangeHandler2 interface, uianimation.iuianimationvariablecurvechangehandler2_oncurvechanged, uianimation/IUIAnimationVariableCurveChangeHandler2::OnCurveChanged
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
 - IUIAnimationVariableCurveChangeHandler2::OnCurveChanged
 - uianimation/IUIAnimationVariableCurveChangeHandler2::OnCurveChanged
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
 - IUIAnimationVariableCurveChangeHandler2.OnCurveChanged
---

# IUIAnimationVariableCurveChangeHandler2::OnCurveChanged


## -description

Handles events that occur when the animation curve of an animation variable changes.

## -parameters

### -param variable [in]

The animation variable for which the animation curve has been updated.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-setvariablecurvechangehandler">IUIAnimationVariable2::SetVariableCurveChangeHandler</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariablecurvechangehandler2">IUIAnimationVariableCurveChangeHandler2</a>