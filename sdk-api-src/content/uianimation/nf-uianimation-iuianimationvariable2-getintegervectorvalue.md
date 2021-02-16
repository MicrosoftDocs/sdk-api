---
UID: NF:uianimation.IUIAnimationVariable2.GetIntegerVectorValue
title: IUIAnimationVariable2::GetIntegerVectorValue (uianimation.h)
description: Gets the integer value of the animation variable for the specified dimension.
helpviewer_keywords: ["GetIntegerVectorValue","GetIntegerVectorValue method [Windows Animation]","GetIntegerVectorValue method [Windows Animation]","IUIAnimationVariable2 interface","IUIAnimationVariable2 interface [Windows Animation]","GetIntegerVectorValue method","IUIAnimationVariable2.GetIntegerVectorValue","IUIAnimationVariable2::GetIntegerVectorValue","uianimation.iuianimationvariable2_getintegervectorvalue","uianimation/IUIAnimationVariable2::GetIntegerVectorValue"]
old-location: uianimation\iuianimationvariable2_getintegervectorvalue.htm
tech.root: UIAnimation
ms.assetid: 63832D4C-C1AB-4073-AE36-1539671F0F59
ms.date: 12/05/2018
ms.keywords: GetIntegerVectorValue, GetIntegerVectorValue method [Windows Animation], GetIntegerVectorValue method [Windows Animation],IUIAnimationVariable2 interface, IUIAnimationVariable2 interface [Windows Animation],GetIntegerVectorValue method, IUIAnimationVariable2.GetIntegerVectorValue, IUIAnimationVariable2::GetIntegerVectorValue, uianimation.iuianimationvariable2_getintegervectorvalue, uianimation/IUIAnimationVariable2::GetIntegerVectorValue
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
 - IUIAnimationVariable2::GetIntegerVectorValue
 - uianimation/IUIAnimationVariable2::GetIntegerVectorValue
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
 - IUIAnimationVariable2.GetIntegerVectorValue
---

# IUIAnimationVariable2::GetIntegerVectorValue


## -description

Gets the integer value of the animation variable for the specified dimension.

## -parameters

### -param value [out]

The value of the animation variable as an integer.

### -param cDimension [in]

The dimension from which to get the value of the animation variable.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>