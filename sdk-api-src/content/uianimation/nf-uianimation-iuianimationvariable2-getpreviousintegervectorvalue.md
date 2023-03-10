---
UID: NF:uianimation.IUIAnimationVariable2.GetPreviousIntegerVectorValue
title: IUIAnimationVariable2::GetPreviousIntegerVectorValue (uianimation.h)
description: Gets the previous integer value of the animation variable for the specified dimension. This is the value of the animation variable before the most recent update.
helpviewer_keywords: ["GetPreviousIntegerVectorValue","GetPreviousIntegerVectorValue method [Windows Animation]","GetPreviousIntegerVectorValue method [Windows Animation]","IUIAnimationVariable2 interface","IUIAnimationVariable2 interface [Windows Animation]","GetPreviousIntegerVectorValue method","IUIAnimationVariable2.GetPreviousIntegerVectorValue","IUIAnimationVariable2::GetPreviousIntegerVectorValue","uianimation.iuianimationvariable2_getpreviousintegervectorvalue","uianimation/IUIAnimationVariable2::GetPreviousIntegerVectorValue"]
old-location: uianimation\iuianimationvariable2_getpreviousintegervectorvalue.htm
tech.root: UIAnimation
ms.assetid: 7061B16A-FB54-4274-8425-551396F353CF
ms.date: 12/05/2018
ms.keywords: GetPreviousIntegerVectorValue, GetPreviousIntegerVectorValue method [Windows Animation], GetPreviousIntegerVectorValue method [Windows Animation],IUIAnimationVariable2 interface, IUIAnimationVariable2 interface [Windows Animation],GetPreviousIntegerVectorValue method, IUIAnimationVariable2.GetPreviousIntegerVectorValue, IUIAnimationVariable2::GetPreviousIntegerVectorValue, uianimation.iuianimationvariable2_getpreviousintegervectorvalue, uianimation/IUIAnimationVariable2::GetPreviousIntegerVectorValue
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
 - IUIAnimationVariable2::GetPreviousIntegerVectorValue
 - uianimation/IUIAnimationVariable2::GetPreviousIntegerVectorValue
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
 - IUIAnimationVariable2.GetPreviousIntegerVectorValue
---

# IUIAnimationVariable2::GetPreviousIntegerVectorValue


## -description

Gets the previous integer value of the animation variable for the specified dimension. This is the value of the animation variable before the most recent update.

## -parameters

### -param previousValue [out]

The previous value of the animation variable as an integer.

### -param cDimension [in]

The dimension from which to get the value of the animation variable.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>