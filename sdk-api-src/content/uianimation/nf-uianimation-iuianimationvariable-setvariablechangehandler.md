---
UID: NF:uianimation.IUIAnimationVariable.SetVariableChangeHandler
title: IUIAnimationVariable::SetVariableChangeHandler (uianimation.h)
description: Specifies a variable change handler. This handler is notified of changes to the value of the animation variable.
helpviewer_keywords: ["IUIAnimationVariable interface [Windows Animation]","SetVariableChangeHandler method","IUIAnimationVariable.SetVariableChangeHandler","IUIAnimationVariable::SetVariableChangeHandler","SetVariableChangeHandler","SetVariableChangeHandler method [Windows Animation]","SetVariableChangeHandler method [Windows Animation]","IUIAnimationVariable interface","uianimation.iuianimationvariable_setvariablechangehandler","uianimation/IUIAnimationVariable::SetVariableChangeHandler"]
old-location: uianimation\iuianimationvariable_setvariablechangehandler.htm
tech.root: UIAnimation
ms.assetid: d773a59f-10a5-41e4-92f1-af72d8d15105
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariable interface [Windows Animation],SetVariableChangeHandler method, IUIAnimationVariable.SetVariableChangeHandler, IUIAnimationVariable::SetVariableChangeHandler, SetVariableChangeHandler, SetVariableChangeHandler method [Windows Animation], SetVariableChangeHandler method [Windows Animation],IUIAnimationVariable interface, uianimation.iuianimationvariable_setvariablechangehandler, uianimation/IUIAnimationVariable::SetVariableChangeHandler
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
 - IUIAnimationVariable::SetVariableChangeHandler
 - uianimation/IUIAnimationVariable::SetVariableChangeHandler
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
 - IUIAnimationVariable.SetVariableChangeHandler
---

# IUIAnimationVariable::SetVariableChangeHandler


## -description

Specifies a variable change handler. This handler is notified of changes to the value of the animation variable.

## -parameters

### -param handler [in, optional]

A variable change handler.  
               
The specified object must implement the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariablechangehandler">IUIAnimationVariableChangeHandler</a> interface or be <b>NULL</b>.

See Remarks.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Passing <b>NULL</b> for the <i>handler</i> parameter causes Windows Animation to release its reference to any handler object you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-shutdown">IUIAnimationManager::Shutdown</a> method.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler">IUIAnimationVariable::SetVariableIntegerChangeHandler</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariablechangehandler">IUIAnimationVariableChangeHandler</a>