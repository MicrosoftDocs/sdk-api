---
UID: NF:uianimation.IUIAnimationVariable2.GetPreviousVectorValue
title: IUIAnimationVariable2::GetPreviousVectorValue (uianimation.h)
description: Gets the previous value of the animation variable for the specified dimension. This is the value of the animation variable before the most recent update.
helpviewer_keywords: ["GetPreviousVectorValue","GetPreviousVectorValue method [Windows Animation]","GetPreviousVectorValue method [Windows Animation]","IUIAnimationVariable2 interface","IUIAnimationVariable2 interface [Windows Animation]","GetPreviousVectorValue method","IUIAnimationVariable2.GetPreviousVectorValue","IUIAnimationVariable2::GetPreviousVectorValue","uianimation.iuianimationvariable2_getpreviousvectorvalue","uianimation/IUIAnimationVariable2::GetPreviousVectorValue"]
old-location: uianimation\iuianimationvariable2_getpreviousvectorvalue.htm
tech.root: UIAnimation
ms.assetid: E6C32B28-A6DE-47FB-8399-CA0B782D8B25
ms.date: 12/05/2018
ms.keywords: GetPreviousVectorValue, GetPreviousVectorValue method [Windows Animation], GetPreviousVectorValue method [Windows Animation],IUIAnimationVariable2 interface, IUIAnimationVariable2 interface [Windows Animation],GetPreviousVectorValue method, IUIAnimationVariable2.GetPreviousVectorValue, IUIAnimationVariable2::GetPreviousVectorValue, uianimation.iuianimationvariable2_getpreviousvectorvalue, uianimation/IUIAnimationVariable2::GetPreviousVectorValue
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
 - IUIAnimationVariable2::GetPreviousVectorValue
 - uianimation/IUIAnimationVariable2::GetPreviousVectorValue
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
 - IUIAnimationVariable2.GetPreviousVectorValue
---

# IUIAnimationVariable2::GetPreviousVectorValue


## -description

Gets the previous value of the animation variable for the specified dimension. This is the value of the animation variable before the most recent update.

## -parameters

### -param previousValue [out]

The previous value of the animation variable.

### -param cDimension [in]

The dimension from which to get the value of the animation variable.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>