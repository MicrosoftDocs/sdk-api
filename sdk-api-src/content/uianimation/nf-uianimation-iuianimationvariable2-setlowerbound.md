---
UID: NF:uianimation.IUIAnimationVariable2.SetLowerBound
title: IUIAnimationVariable2::SetLowerBound (uianimation.h)
description: Sets the lower bound (floor) for the value of the animation variable. The value of the animation variable should not fall below the specified value.
helpviewer_keywords: ["IUIAnimationVariable2 interface [Windows Animation]","SetLowerBound method","IUIAnimationVariable2.SetLowerBound","IUIAnimationVariable2::SetLowerBound","SetLowerBound","SetLowerBound method [Windows Animation]","SetLowerBound method [Windows Animation]","IUIAnimationVariable2 interface","uianimation.iuianimationvariable2_setlowerbound","uianimation/IUIAnimationVariable2::SetLowerBound"]
old-location: uianimation\iuianimationvariable2_setlowerbound.htm
tech.root: UIAnimation
ms.assetid: 5149778F-C78D-49C2-8C2E-DBAB00B78DE8
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariable2 interface [Windows Animation],SetLowerBound method, IUIAnimationVariable2.SetLowerBound, IUIAnimationVariable2::SetLowerBound, SetLowerBound, SetLowerBound method [Windows Animation], SetLowerBound method [Windows Animation],IUIAnimationVariable2 interface, uianimation.iuianimationvariable2_setlowerbound, uianimation/IUIAnimationVariable2::SetLowerBound
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
 - IUIAnimationVariable2::SetLowerBound
 - uianimation/IUIAnimationVariable2::SetLowerBound
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
 - IUIAnimationVariable2.SetLowerBound
---

# IUIAnimationVariable2::SetLowerBound


## -description

Sets the lower bound (floor) for the value of the animation variable. The value of the animation variable should not fall below the specified value.

## -parameters

### -param bound [in]

The lower bound for the value of the animation variable.

## -returns

Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>