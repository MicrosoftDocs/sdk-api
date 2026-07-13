---
UID: NN:uianimation.IUIAnimationVariableChangeHandler2
title: IUIAnimationVariableChangeHandler2 (uianimation.h)
description: Defines a method for handling animation variable update events. IUIAnimationVariableChangeHandler2 handles events that occur in a specified dimension.
helpviewer_keywords: ["IUIAnimationVariableChangeHandler2","IUIAnimationVariableChangeHandler2 interface [Windows Animation]","IUIAnimationVariableChangeHandler2 interface [Windows Animation]","described","uianimation.iuianimationvariablechangehandler2","uianimation/IUIAnimationVariableChangeHandler2"]
old-location: uianimation\iuianimationvariablechangehandler2.htm
tech.root: UIAnimation
ms.assetid: A8D3B617-43D6-4541-AE98-1332DB5205CE
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariableChangeHandler2, IUIAnimationVariableChangeHandler2 interface [Windows Animation], IUIAnimationVariableChangeHandler2 interface [Windows Animation],described, uianimation.iuianimationvariablechangehandler2, uianimation/IUIAnimationVariableChangeHandler2
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
 - IUIAnimationVariableChangeHandler2
 - uianimation/IUIAnimationVariableChangeHandler2
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
 - IUIAnimationVariableChangeHandler2
---

# IUIAnimationVariableChangeHandler2 interface


## -description

Defines a method for handling animation variable update events. <b>IUIAnimationVariableChangeHandler2</b> handles events that occur in a specified dimension.

## -inheritance

The <b>IUIAnimationVariableChangeHandler2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationVariableChangeHandler2</b> also has these types of members:

## -remarks

The <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariablechangehandler2-onvaluechanged">OnValueChanged</a> method receives animation variable value updates as <b>DOUBLE</b> values.
      
To receive value updates as <b>INT32</b> values, use the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariableintegerchangehandler2-onintegervaluechanged">IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged</a> method.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getvalue">IUIAnimationVariable2::GetValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-setvariablechangehandler">IUIAnimationVariable2::SetVariableChangeHandler</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariableintegerchangehandler2">IUIAnimationVariableIntegerChangeHandler2</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/UIAnimation/-interfaces-main">Interfaces</a>
