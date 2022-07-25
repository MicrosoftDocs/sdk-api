---
UID: NN:uianimation.IUIAnimationVariableIntegerChangeHandler
title: IUIAnimationVariableIntegerChangeHandler (uianimation.h)
description: Defines a method for handling animation variable update events.
helpviewer_keywords: ["IUIAnimationVariableIntegerChangeHandler","IUIAnimationVariableIntegerChangeHandler interface [Windows Animation]","IUIAnimationVariableIntegerChangeHandler interface [Windows Animation]","described","uianimation.iuianimationvariableintegerchangehandler","uianimation/IUIAnimationVariableIntegerChangeHandler"]
old-location: uianimation\iuianimationvariableintegerchangehandler.htm
tech.root: UIAnimation
ms.assetid: acd9ff0f-e2e4-4711-9d9c-54624f170ec6
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariableIntegerChangeHandler, IUIAnimationVariableIntegerChangeHandler interface [Windows Animation], IUIAnimationVariableIntegerChangeHandler interface [Windows Animation],described, uianimation.iuianimationvariableintegerchangehandler, uianimation/IUIAnimationVariableIntegerChangeHandler
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
 - IUIAnimationVariableIntegerChangeHandler
 - uianimation/IUIAnimationVariableIntegerChangeHandler
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
 - IUIAnimationVariableIntegerChangeHandler
---

# IUIAnimationVariableIntegerChangeHandler interface


## -description

Defines a method for handling animation variable update events.

## -inheritance

The <b>IUIAnimationVariableIntegerChangeHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationVariableIntegerChangeHandler</b> also has these types of members:

## -remarks

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged">OnIntegerValueChanged</a> receives animation variable value updates as <b>INT32</b> values.
      
 To receive value updates as <b>DOUBLE</b> values, use the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged">IUIAnimationVariableChangeHandler::OnValueChanged</a> method.

## -see-also

<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getintegervalue">IUIAnimationVariable::GetIntegerValue</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler">IUIAnimationVariable::SetVariableIntegerChangeHandler</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
