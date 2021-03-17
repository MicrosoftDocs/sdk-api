---
UID: NF:uianimation.IUIAnimationVariable2.GetFinalVectorValue
title: IUIAnimationVariable2::GetFinalVectorValue (uianimation.h)
description: Gets the final value of the animation variable for the specified dimension. This is the value after all currently scheduled animations have completed.
helpviewer_keywords: ["GetFinalVectorValue","GetFinalVectorValue method [Windows Animation]","GetFinalVectorValue method [Windows Animation]","IUIAnimationVariable2 interface","IUIAnimationVariable2 interface [Windows Animation]","GetFinalVectorValue method","IUIAnimationVariable2.GetFinalVectorValue","IUIAnimationVariable2::GetFinalVectorValue","uianimation.iuianimationvariable2_getfinalvectorvalue","uianimation/IUIAnimationVariable2::GetFinalVectorValue"]
old-location: uianimation\iuianimationvariable2_getfinalvectorvalue.htm
tech.root: UIAnimation
ms.assetid: 2794B65F-0461-4E0F-832D-CEC9BEE60B6E
ms.date: 12/05/2018
ms.keywords: GetFinalVectorValue, GetFinalVectorValue method [Windows Animation], GetFinalVectorValue method [Windows Animation],IUIAnimationVariable2 interface, IUIAnimationVariable2 interface [Windows Animation],GetFinalVectorValue method, IUIAnimationVariable2.GetFinalVectorValue, IUIAnimationVariable2::GetFinalVectorValue, uianimation.iuianimationvariable2_getfinalvectorvalue, uianimation/IUIAnimationVariable2::GetFinalVectorValue
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
 - IUIAnimationVariable2::GetFinalVectorValue
 - uianimation/IUIAnimationVariable2::GetFinalVectorValue
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
 - IUIAnimationVariable2.GetFinalVectorValue
---

# IUIAnimationVariable2::GetFinalVectorValue


## -description

Gets the final value of the animation variable for the specified dimension. This is the value after all currently scheduled animations have completed.

## -parameters

### -param finalValue [out]

The final value of the animation variable.

### -param cDimension [in]

The dimension from which to get the value of the animation variable.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>