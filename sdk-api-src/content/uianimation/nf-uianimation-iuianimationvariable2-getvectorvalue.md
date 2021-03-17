---
UID: NF:uianimation.IUIAnimationVariable2.GetVectorValue
title: IUIAnimationVariable2::GetVectorValue (uianimation.h)
description: Gets the value of the animation variable in the specified dimension.
helpviewer_keywords: ["GetVectorValue","GetVectorValue method [Windows Animation]","GetVectorValue method [Windows Animation]","IUIAnimationVariable2 interface","IUIAnimationVariable2 interface [Windows Animation]","GetVectorValue method","IUIAnimationVariable2.GetVectorValue","IUIAnimationVariable2::GetVectorValue","uianimation.iuianimationvariable2_getvectorvalue","uianimation/IUIAnimationVariable2::GetVectorValue"]
old-location: uianimation\iuianimationvariable2_getvectorvalue.htm
tech.root: UIAnimation
ms.assetid: B53EDC6C-7B1E-4CDE-8F4A-5B0601892630
ms.date: 12/05/2018
ms.keywords: GetVectorValue, GetVectorValue method [Windows Animation], GetVectorValue method [Windows Animation],IUIAnimationVariable2 interface, IUIAnimationVariable2 interface [Windows Animation],GetVectorValue method, IUIAnimationVariable2.GetVectorValue, IUIAnimationVariable2::GetVectorValue, uianimation.iuianimationvariable2_getvectorvalue, uianimation/IUIAnimationVariable2::GetVectorValue
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
 - IUIAnimationVariable2::GetVectorValue
 - uianimation/IUIAnimationVariable2::GetVectorValue
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
 - IUIAnimationVariable2.GetVectorValue
---

# IUIAnimationVariable2::GetVectorValue


## -description

Gets the value of the animation variable in the specified dimension.

## -parameters

### -param value [out]

The value of the animation variable.

### -param cDimension [in]

The dimension from which to get the value of the animation variable.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>