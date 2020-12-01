---
UID: NF:uianimation.IUIAnimationVariable2.SetLowerBoundVector
title: IUIAnimationVariable2::SetLowerBoundVector (uianimation.h)
description: Sets the lower bound (floor) value of each specified dimension for the animation variable. The value of each animation variable should not fall below its lower bound.
helpviewer_keywords: ["IUIAnimationVariable2 interface [Windows Animation]","SetLowerBoundVector method","IUIAnimationVariable2.SetLowerBoundVector","IUIAnimationVariable2::SetLowerBoundVector","SetLowerBoundVector","SetLowerBoundVector method [Windows Animation]","SetLowerBoundVector method [Windows Animation]","IUIAnimationVariable2 interface","uianimation.iuianimationvariable2_setlowerboundvector","uianimation/IUIAnimationVariable2::SetLowerBoundVector"]
old-location: uianimation\iuianimationvariable2_setlowerboundvector.htm
tech.root: UIAnimation
ms.assetid: CB7D30BF-D22C-40EB-A530-035CED1BDAF0
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariable2 interface [Windows Animation],SetLowerBoundVector method, IUIAnimationVariable2.SetLowerBoundVector, IUIAnimationVariable2::SetLowerBoundVector, SetLowerBoundVector, SetLowerBoundVector method [Windows Animation], SetLowerBoundVector method [Windows Animation],IUIAnimationVariable2 interface, uianimation.iuianimationvariable2_setlowerboundvector, uianimation/IUIAnimationVariable2::SetLowerBoundVector
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
 - IUIAnimationVariable2::SetLowerBoundVector
 - uianimation/IUIAnimationVariable2::SetLowerBoundVector
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
 - IUIAnimationVariable2.SetLowerBoundVector
---

# IUIAnimationVariable2::SetLowerBoundVector


## -description

Sets the lower bound (floor) value of each specified dimension for the animation variable. The value of each animation variable should not fall below its lower bound.

## -parameters

### -param bound [in]

A vector (of size <i>cDimension</i>) that contains  the lower bound values of each dimension.

### -param cDimension [in]

The number of dimensions that require lower bound values. This parameter specifies the number of values listed in <i>bound</i>.

## -returns

Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>