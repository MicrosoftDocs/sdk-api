---
UID: NN:uianimation.IUIAnimationVariableIntegerChangeHandler
title: IUIAnimationVariableIntegerChangeHandler (uianimation.h)
author: windows-sdk-content
description: Defines a method for handling animation variable update events.
old-location: uianimation\iuianimationvariableintegerchangehandler.htm
tech.root: UIAnimation
ms.assetid: acd9ff0f-e2e4-4711-9d9c-54624f170ec6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariableIntegerChangeHandler, IUIAnimationVariableIntegerChangeHandler interface [Windows Animation], IUIAnimationVariableIntegerChangeHandler interface [Windows Animation],described, uianimation.iuianimationvariableintegerchangehandler, uianimation/IUIAnimationVariableIntegerChangeHandler
ms.topic: interface
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
 - IUIAnimationVariableIntegerChangeHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationVariableIntegerChangeHandler interface


## -description


Defines a method for handling animation variable update events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationVariableIntegerChangeHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationVariableIntegerChangeHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationVariableIntegerChangeHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged">OnIntegerValueChanged</a>
</td>
<td align="left" width="63%">
Handles events that occur when the value of an animation variable changes.

</td>
</tr>
</table> 


## -remarks




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariableintegerchangehandler-onintegervaluechanged">OnIntegerValueChanged</a> receives animation variable value updates as <b>INT32</b> values.
      
         To receive value updates as <b>DOUBLE</b> values, use
         the <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariablechangehandler-onvaluechanged">IUIAnimationVariableChangeHandler::OnValueChanged</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-getintegervalue">IUIAnimationVariable::GetIntegerValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable-setvariableintegerchangehandler">IUIAnimationVariable::SetVariableIntegerChangeHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

