---
UID: NF:uianimation.IUIAnimationVariable2.GetPreviousIntegerValue
title: IUIAnimationVariable2::GetPreviousIntegerValue (uianimation.h)
description: Gets the previous integer value of the animation variable in the specified dimension. This is the value of the animation variable before the most recent update.
helpviewer_keywords: ["GetPreviousIntegerValue","GetPreviousIntegerValue method [Windows Animation]","GetPreviousIntegerValue method [Windows Animation]","IUIAnimationVariable2 interface","IUIAnimationVariable2 interface [Windows Animation]","GetPreviousIntegerValue method","IUIAnimationVariable2.GetPreviousIntegerValue","IUIAnimationVariable2::GetPreviousIntegerValue","uianimation.iuianimationvariable2_getpreviousintegervalue","uianimation/IUIAnimationVariable2::GetPreviousIntegerValue"]
old-location: uianimation\iuianimationvariable2_getpreviousintegervalue.htm
tech.root: UIAnimation
ms.assetid: 8B25BE8D-B12F-44B4-AFBF-3E6994BA0771
ms.date: 12/05/2018
ms.keywords: GetPreviousIntegerValue, GetPreviousIntegerValue method [Windows Animation], GetPreviousIntegerValue method [Windows Animation],IUIAnimationVariable2 interface, IUIAnimationVariable2 interface [Windows Animation],GetPreviousIntegerValue method, IUIAnimationVariable2.GetPreviousIntegerValue, IUIAnimationVariable2::GetPreviousIntegerValue, uianimation.iuianimationvariable2_getpreviousintegervalue, uianimation/IUIAnimationVariable2::GetPreviousIntegerValue
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
 - IUIAnimationVariable2::GetPreviousIntegerValue
 - uianimation/IUIAnimationVariable2::GetPreviousIntegerValue
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
 - IUIAnimationVariable2.GetPreviousIntegerValue
---

# IUIAnimationVariable2::GetPreviousIntegerValue


## -description

Gets the previous integer value of the animation variable in the specified dimension. This is the value of the animation variable before the most recent update.

## -parameters

### -param previousValue [out]

The previous value of the animation variable as an integer.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>