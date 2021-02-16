---
UID: NF:uianimation.IUIAnimationVariable2.SetUpperBound
title: IUIAnimationVariable2::SetUpperBound (uianimation.h)
description: Sets the upper bound (ceiling) for the value of the animation variable. The value of the animation variable should not rise above the specified value.
helpviewer_keywords: ["IUIAnimationVariable2 interface [Windows Animation]","SetUpperBound method","IUIAnimationVariable2.SetUpperBound","IUIAnimationVariable2::SetUpperBound","SetUpperBound","SetUpperBound method [Windows Animation]","SetUpperBound method [Windows Animation]","IUIAnimationVariable2 interface","uianimation.iuianimationvariable2_setupperbound","uianimation/IUIAnimationVariable2::SetUpperBound"]
old-location: uianimation\iuianimationvariable2_setupperbound.htm
tech.root: UIAnimation
ms.assetid: AE142CD9-61BB-427A-A40B-42EFDD0B5CAD
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariable2 interface [Windows Animation],SetUpperBound method, IUIAnimationVariable2.SetUpperBound, IUIAnimationVariable2::SetUpperBound, SetUpperBound, SetUpperBound method [Windows Animation], SetUpperBound method [Windows Animation],IUIAnimationVariable2 interface, uianimation.iuianimationvariable2_setupperbound, uianimation/IUIAnimationVariable2::SetUpperBound
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
 - IUIAnimationVariable2::SetUpperBound
 - uianimation/IUIAnimationVariable2::SetUpperBound
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
 - IUIAnimationVariable2.SetUpperBound
---

# IUIAnimationVariable2::SetUpperBound


## -description

Sets the upper bound (ceiling) for the value of the animation variable. The value of the animation variable should not rise above the specified value.

## -parameters

### -param bound [in]

The upper bound for the value of the animation variable.

## -returns

Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>