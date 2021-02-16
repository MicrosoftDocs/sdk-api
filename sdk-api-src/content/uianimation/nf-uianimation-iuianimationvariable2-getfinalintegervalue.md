---
UID: NF:uianimation.IUIAnimationVariable2.GetFinalIntegerValue
title: IUIAnimationVariable2::GetFinalIntegerValue (uianimation.h)
description: Gets the final integer value of the animation variable. This is the value after all currently scheduled animations have completed.
helpviewer_keywords: ["GetFinalIntegerValue","GetFinalIntegerValue method [Windows Animation]","GetFinalIntegerValue method [Windows Animation]","IUIAnimationVariable2 interface","IUIAnimationVariable2 interface [Windows Animation]","GetFinalIntegerValue method","IUIAnimationVariable2.GetFinalIntegerValue","IUIAnimationVariable2::GetFinalIntegerValue","uianimation.iuianimationvariable2_getfinalintegervalue","uianimation/IUIAnimationVariable2::GetFinalIntegerValue"]
old-location: uianimation\iuianimationvariable2_getfinalintegervalue.htm
tech.root: UIAnimation
ms.assetid: 290EC1D8-007D-44A0-B3F8-384A9594FDC4
ms.date: 12/05/2018
ms.keywords: GetFinalIntegerValue, GetFinalIntegerValue method [Windows Animation], GetFinalIntegerValue method [Windows Animation],IUIAnimationVariable2 interface, IUIAnimationVariable2 interface [Windows Animation],GetFinalIntegerValue method, IUIAnimationVariable2.GetFinalIntegerValue, IUIAnimationVariable2::GetFinalIntegerValue, uianimation.iuianimationvariable2_getfinalintegervalue, uianimation/IUIAnimationVariable2::GetFinalIntegerValue
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
 - IUIAnimationVariable2::GetFinalIntegerValue
 - uianimation/IUIAnimationVariable2::GetFinalIntegerValue
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
 - IUIAnimationVariable2.GetFinalIntegerValue
---

# IUIAnimationVariable2::GetFinalIntegerValue


## -description

Gets the final integer value of the animation variable. This is the value after all currently scheduled animations have completed.

## -parameters

### -param finalValue [out]

The final value of the animation variable as an integer.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>