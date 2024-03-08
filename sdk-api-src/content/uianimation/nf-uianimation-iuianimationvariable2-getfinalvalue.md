---
UID: NF:uianimation.IUIAnimationVariable2.GetFinalValue
title: IUIAnimationVariable2::GetFinalValue (uianimation.h)
description: Gets the final value of the animation variable. This is the value after all currently scheduled animations have completed. (IUIAnimationVariable2.GetFinalValue)
helpviewer_keywords: ["GetFinalValue","GetFinalValue method [Windows Animation]","GetFinalValue method [Windows Animation]","IUIAnimationVariable2 interface","IUIAnimationVariable2 interface [Windows Animation]","GetFinalValue method","IUIAnimationVariable2.GetFinalValue","IUIAnimationVariable2::GetFinalValue","uianimation.iuianimationvariable2_getfinalvalue","uianimation/IUIAnimationVariable2::GetFinalValue"]
old-location: uianimation\iuianimationvariable2_getfinalvalue.htm
tech.root: UIAnimation
ms.assetid: FF39BE67-AED7-4B67-ABAF-D5D51619F0D3
ms.date: 12/05/2018
ms.keywords: GetFinalValue, GetFinalValue method [Windows Animation], GetFinalValue method [Windows Animation],IUIAnimationVariable2 interface, IUIAnimationVariable2 interface [Windows Animation],GetFinalValue method, IUIAnimationVariable2.GetFinalValue, IUIAnimationVariable2::GetFinalValue, uianimation.iuianimationvariable2_getfinalvalue, uianimation/IUIAnimationVariable2::GetFinalValue
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
 - IUIAnimationVariable2::GetFinalValue
 - uianimation/IUIAnimationVariable2::GetFinalValue
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
 - IUIAnimationVariable2.GetFinalValue
---

# IUIAnimationVariable2::GetFinalValue


## -description

Gets the final value of the animation variable. This is the value after all currently scheduled animations have completed.

## -parameters

### -param finalValue [out]

The final value of the animation variable.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable2">IUIAnimationVariable2</a>
