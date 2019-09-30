---
UID: NN:uianimation.IUIAnimationVariableChangeHandler
title: IUIAnimationVariableChangeHandler (uianimation.h)
author: windows-sdk-content
description: Defines a method for handling events related to animation variable updates.
old-location: uianimation\iuianimationvariablechangehandler.htm
tech.root: UIAnimation
ms.assetid: 2288b256-aaf4-44fe-9ad1-f05ef7b0e30b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariableChangeHandler, IUIAnimationVariableChangeHandler interface [Windows Animation], IUIAnimationVariableChangeHandler interface [Windows Animation],described, uianimation.iuianimationvariablechangehandler, uianimation/IUIAnimationVariableChangeHandler
ms.topic: interface
f1_keywords: 
 - "uianimation/IUIAnimationVariableChangeHandler"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAnimation.dll
api_name:
 - IUIAnimationVariableChangeHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationVariableChangeHandler interface


## -description


Defines a method for handling events related to animation variable updates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationVariableChangeHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationVariableChangeHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationVariableChangeHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged">OnValueChanged</a>
</td>
<td align="left" width="63%">
Handles events that occur when the value of an animation variable changes.

</td>
</tr>
</table> 


## -remarks




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged">OnValueChanged</a> receives animation variable value updates as 
         <b>DOUBLE</b> values.
      
         To receive value updates as <b>INT32</b> values, use
         <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged">IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getvalue">IUIAnimationVariable::GetValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setvariablechangehandler">IUIAnimationVariable::SetVariableChangeHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

