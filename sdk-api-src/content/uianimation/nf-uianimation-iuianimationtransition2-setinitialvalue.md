---
UID: NF:uianimation.IUIAnimationTransition2.SetInitialValue
title: IUIAnimationTransition2::SetInitialValue (uianimation.h)
description: Sets the initial value of the transition.
helpviewer_keywords: ["IUIAnimationTransition2 interface [Windows Animation]","SetInitialValue method","IUIAnimationTransition2.SetInitialValue","IUIAnimationTransition2::SetInitialValue","SetInitialValue","SetInitialValue method [Windows Animation]","SetInitialValue method [Windows Animation]","IUIAnimationTransition2 interface","uianimation.iuianimationtransition2_setinitialvalue","uianimation/IUIAnimationTransition2::SetInitialValue"]
old-location: uianimation\iuianimationtransition2_setinitialvalue.htm
tech.root: UIAnimation
ms.assetid: 813224BE-369D-4D65-AA12-AEE590627F40
ms.date: 12/05/2018
ms.keywords: IUIAnimationTransition2 interface [Windows Animation],SetInitialValue method, IUIAnimationTransition2.SetInitialValue, IUIAnimationTransition2::SetInitialValue, SetInitialValue, SetInitialValue method [Windows Animation], SetInitialValue method [Windows Animation],IUIAnimationTransition2 interface, uianimation.iuianimationtransition2_setinitialvalue, uianimation/IUIAnimationTransition2::SetInitialValue
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
 - IUIAnimationTransition2::SetInitialValue
 - uianimation/IUIAnimationTransition2::SetInitialValue
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
 - IUIAnimationTransition2.SetInitialValue
---

# IUIAnimationTransition2::SetInitialValue


## -description

Sets the initial value of the transition.

## -parameters

### -param value [in]

The initial value for the transition.

## -returns

Returns S_OK if successful; otherwise an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Do not call this method after the transition has been added to a storyboard.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition2">IUIAnimationTransition2</a>