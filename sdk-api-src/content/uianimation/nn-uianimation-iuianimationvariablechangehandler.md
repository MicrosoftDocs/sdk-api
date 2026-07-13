---
UID: NN:uianimation.IUIAnimationVariableChangeHandler
title: IUIAnimationVariableChangeHandler (uianimation.h)
description: Defines a method for handling events related to animation variable updates.
helpviewer_keywords: ["IUIAnimationVariableChangeHandler","IUIAnimationVariableChangeHandler interface [Windows Animation]","IUIAnimationVariableChangeHandler interface [Windows Animation]","described","uianimation.iuianimationvariablechangehandler","uianimation/IUIAnimationVariableChangeHandler"]
old-location: uianimation\iuianimationvariablechangehandler.htm
tech.root: UIAnimation
ms.assetid: 2288b256-aaf4-44fe-9ad1-f05ef7b0e30b
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariableChangeHandler, IUIAnimationVariableChangeHandler interface [Windows Animation], IUIAnimationVariableChangeHandler interface [Windows Animation],described, uianimation.iuianimationvariablechangehandler, uianimation/IUIAnimationVariableChangeHandler
req.header: uianimation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update for Windows Vista [desktop apps \| UWP apps]
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
 - IUIAnimationVariableChangeHandler
 - uianimation/IUIAnimationVariableChangeHandler
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
 - IUIAnimationVariableChangeHandler
---

# IUIAnimationVariableChangeHandler interface


## -description

Defines a method for handling events related to animation variable updates.

## -inheritance

The <b>IUIAnimationVariableChangeHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationVariableChangeHandler</b> also has these types of members:

## -remarks

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged">OnValueChanged</a> receives animation variable value updates as <b>DOUBLE</b> values.
      
To receive value updates as <b>INT32</b> values, use <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged">IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged</a>.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getvalue">IUIAnimationVariable::GetValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setvariablechangehandler">IUIAnimationVariable::SetVariableChangeHandler</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
