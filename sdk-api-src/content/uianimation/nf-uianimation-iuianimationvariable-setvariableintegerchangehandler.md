---
UID: NF:uianimation.IUIAnimationVariable.SetVariableIntegerChangeHandler
title: IUIAnimationVariable::SetVariableIntegerChangeHandler (uianimation.h)
description: Specifies an integer variable change handler. This handler is notified of changes to the integer value of the animation variable.
helpviewer_keywords: ["IUIAnimationVariable interface [Windows Animation]","SetVariableIntegerChangeHandler method","IUIAnimationVariable.SetVariableIntegerChangeHandler","IUIAnimationVariable::SetVariableIntegerChangeHandler","SetVariableIntegerChangeHandler","SetVariableIntegerChangeHandler method [Windows Animation]","SetVariableIntegerChangeHandler method [Windows Animation]","IUIAnimationVariable interface","uianimation.iuianimationvariable_setvariableintegerchangehandler","uianimation/IUIAnimationVariable::SetVariableIntegerChangeHandler"]
old-location: uianimation\iuianimationvariable_setvariableintegerchangehandler.htm
tech.root: UIAnimation
ms.assetid: 8dc20701-0808-4308-92fc-8be6c4b039ca
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariable interface [Windows Animation],SetVariableIntegerChangeHandler method, IUIAnimationVariable.SetVariableIntegerChangeHandler, IUIAnimationVariable::SetVariableIntegerChangeHandler, SetVariableIntegerChangeHandler, SetVariableIntegerChangeHandler method [Windows Animation], SetVariableIntegerChangeHandler method [Windows Animation],IUIAnimationVariable interface, uianimation.iuianimationvariable_setvariableintegerchangehandler, uianimation/IUIAnimationVariable::SetVariableIntegerChangeHandler
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
 - IUIAnimationVariable::SetVariableIntegerChangeHandler
 - uianimation/IUIAnimationVariable::SetVariableIntegerChangeHandler
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
 - IUIAnimationVariable.SetVariableIntegerChangeHandler
---

# IUIAnimationVariable::SetVariableIntegerChangeHandler


## -description

Specifies an integer variable change handler. This handler is notified of changes to the integer value of the animation variable.

## -parameters

### -param handler [in, optional]

An integer variable change handler.  
               
The specified object must implement the <a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariableintegerchangehandler">IUIAnimationVariableIntegerChangeHandler</a> interface or be NULL.

See Remarks.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/UIAnimation/uianimation-error-codes">Windows Animation Error Codes</a> for a list of error codes.

## -remarks

Passing NULL for the <i>handler</i> parameter causes Windows Animation to release its reference to any handler object you passed in earlier. This technique can be essential for breaking reference cycles without having to call the <a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationmanager-shutdown">IUIAnimationManager::Shutdown</a> method.


<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged">IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged</a> is called only if the rounded value has changed since the last update.

## -see-also

<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariable">IUIAnimationVariable</a>



<a href="/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setvariablechangehandler">IUIAnimationVariable::SetVariableChangeHandler</a>



<a href="/windows/desktop/api/uianimation/nn-uianimation-iuianimationvariablechangehandler">IUIAnimationVariableChangeHandler</a>