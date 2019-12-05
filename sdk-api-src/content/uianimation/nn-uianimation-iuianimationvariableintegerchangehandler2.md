---
UID: NN:uianimation.IUIAnimationVariableIntegerChangeHandler2
title: IUIAnimationVariableIntegerChangeHandler2 (uianimation.h)
description: Defines a method for handling animation variable update events. IUIAnimationVariableIntegerChangeHandler2 handles events that occur in a specified dimension.
old-location: uianimation\iuianimationvariableintegerchangehandler2.htm
tech.root: UIAnimation
ms.assetid: 778BE01B-360C-431C-9515-DE43B4F2B77D
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariableIntegerChangeHandler2, IUIAnimationVariableIntegerChangeHandler2 interface [Windows Animation], IUIAnimationVariableIntegerChangeHandler2 interface [Windows Animation],described, uianimation.iuianimationvariableintegerchangehandler2, uianimation/IUIAnimationVariableIntegerChangeHandler2
ms.topic: interface
f1_keywords:
- uianimation/IUIAnimationVariableIntegerChangeHandler2
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAnimation.dll
api_name:
- IUIAnimationVariableIntegerChangeHandler2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationVariableIntegerChangeHandler2 interface


## -description


Defines a method for handling animation variable update events. <b>IUIAnimationVariableIntegerChangeHandler2</b> handles events that occur in a specified dimension.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationVariableIntegerChangeHandler2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationVariableIntegerChangeHandler2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationVariableIntegerChangeHandler2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariableintegerchangehandler2-onintegervaluechanged">OnIntegerValueChanged</a>
</td>
<td align="left" width="63%">
Handles events that occur when the integer value of an animation variable changes in the specified dimension.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getintegervalue">IUIAnimationVariable2::GetIntegerValue</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-setvariableintegerchangehandler">IUIAnimationVariable2::SetVariableIntegerChangeHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/UIAnimation/-interfaces-main">Interfaces</a>
 

 

