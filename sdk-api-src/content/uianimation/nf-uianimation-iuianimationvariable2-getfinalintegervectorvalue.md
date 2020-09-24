---
UID: NF:uianimation.IUIAnimationVariable2.GetFinalIntegerVectorValue
title: IUIAnimationVariable2::GetFinalIntegerVectorValue (uianimation.h)
description: Gets the final integer value of the animation variable for the specified dimension. This is the value after all currently scheduled animations have completed.
helpviewer_keywords: ["GetFinalIntegerVectorValue","GetFinalIntegerVectorValue method [Windows Animation]","GetFinalIntegerVectorValue method [Windows Animation]","IUIAnimationVariable2 interface","IUIAnimationVariable2 interface [Windows Animation]","GetFinalIntegerVectorValue method","IUIAnimationVariable2.GetFinalIntegerVectorValue","IUIAnimationVariable2::GetFinalIntegerVectorValue","uianimation.iuianimationvariable2_getfinalintegervectorvalue","uianimation/IUIAnimationVariable2::GetFinalIntegerVectorValue"]
old-location: uianimation\iuianimationvariable2_getfinalintegervectorvalue.htm
tech.root: UIAnimation
ms.assetid: 191DA982-E3F1-4E37-A4D8-7813201E6B6B
ms.date: 12/05/2018
ms.keywords: GetFinalIntegerVectorValue, GetFinalIntegerVectorValue method [Windows Animation], GetFinalIntegerVectorValue method [Windows Animation],IUIAnimationVariable2 interface, IUIAnimationVariable2 interface [Windows Animation],GetFinalIntegerVectorValue method, IUIAnimationVariable2.GetFinalIntegerVectorValue, IUIAnimationVariable2::GetFinalIntegerVectorValue, uianimation.iuianimationvariable2_getfinalintegervectorvalue, uianimation/IUIAnimationVariable2::GetFinalIntegerVectorValue
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
 - IUIAnimationVariable2::GetFinalIntegerVectorValue
 - uianimation/IUIAnimationVariable2::GetFinalIntegerVectorValue
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
 - IUIAnimationVariable2.GetFinalIntegerVectorValue
---

# IUIAnimationVariable2::GetFinalIntegerVectorValue


## -description

Gets the final integer value of the animation variable for the specified dimension. This is the value after all currently scheduled animations have completed.

## -parameters

### -param finalValue [out]

The final value of the animation variable as an integer.

### -param cDimension [in]

The dimension from which to get the value of the animation variable.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>