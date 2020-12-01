---
UID: NF:uianimation.IUIAnimationVariable2.SetUpperBoundVector
title: IUIAnimationVariable2::SetUpperBoundVector (uianimation.h)
description: Sets the upper bound (ceiling) value of each specified dimension for the animation variable. The value of each animation variable should not rise above its upper bound.
helpviewer_keywords: ["IUIAnimationVariable2 interface [Windows Animation]","SetUpperBoundVector method","IUIAnimationVariable2.SetUpperBoundVector","IUIAnimationVariable2::SetUpperBoundVector","SetUpperBoundVector","SetUpperBoundVector method [Windows Animation]","SetUpperBoundVector method [Windows Animation]","IUIAnimationVariable2 interface","uianimation.iuianimationvariable2_setupperboundvector","uianimation/IUIAnimationVariable2::SetUpperBoundVector"]
old-location: uianimation\iuianimationvariable2_setupperboundvector.htm
tech.root: UIAnimation
ms.assetid: 776CDF6F-F93F-44DC-93D7-79D3A866FAF2
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariable2 interface [Windows Animation],SetUpperBoundVector method, IUIAnimationVariable2.SetUpperBoundVector, IUIAnimationVariable2::SetUpperBoundVector, SetUpperBoundVector, SetUpperBoundVector method [Windows Animation], SetUpperBoundVector method [Windows Animation],IUIAnimationVariable2 interface, uianimation.iuianimationvariable2_setupperboundvector, uianimation/IUIAnimationVariable2::SetUpperBoundVector
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
 - IUIAnimationVariable2::SetUpperBoundVector
 - uianimation/IUIAnimationVariable2::SetUpperBoundVector
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
 - IUIAnimationVariable2.SetUpperBoundVector
---

# IUIAnimationVariable2::SetUpperBoundVector


## -description

Sets the upper bound (ceiling) value of each specified dimension for the animation variable. The value of each animation variable should not rise above its upper bound.

## -parameters

### -param bound [in]

A vector (of size <i>cDimension</i>) that contains  the upper bound values of each dimension.

### -param cDimension [in]

The number of dimensions that require upper bound values. This parameter specifies the number of values listed in <i>bound</i>.

## -returns

Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>