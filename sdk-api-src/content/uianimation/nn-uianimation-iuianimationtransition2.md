---
UID: NN:uianimation.IUIAnimationTransition2
title: IUIAnimationTransition2 (uianimation.h)
description: Extends the IUIAnimationTransition interface that defines a transition. An IUIAnimationTransition2 transition determines how an animation variable changes over time in a given dimension.
helpviewer_keywords: ["IUIAnimationTransition2","IUIAnimationTransition2 interface [Windows Animation]","IUIAnimationTransition2 interface [Windows Animation]","described","uianimation.iuianimationtransition2","uianimation/IUIAnimationTransition2"]
old-location: uianimation\iuianimationtransition2.htm
tech.root: UIAnimation
ms.assetid: CACB8053-7716-42E4-9C3B-9CCBBC30808A
ms.date: 12/05/2018
ms.keywords: IUIAnimationTransition2, IUIAnimationTransition2 interface [Windows Animation], IUIAnimationTransition2 interface [Windows Animation],described, uianimation.iuianimationtransition2, uianimation/IUIAnimationTransition2
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
 - IUIAnimationTransition2
 - uianimation/IUIAnimationTransition2
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
 - IUIAnimationTransition2
---

# IUIAnimationTransition2 interface


## -description

Extends the <a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationtransition">IUIAnimationTransition</a> interface that defines a transition. An  <b>IUIAnimationTransition2</b> transition determines how an animation variable  changes over time in a given dimension.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationTransition2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationTransition2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationTransition2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition2-getdimension">GetDimension</a>
</td>
<td align="left" width="63%">
Gets the number of dimensions in which the animation variable has a transition specified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition2-getduration">GetDuration</a>
</td>
<td align="left" width="63%">
Gets the duration of the transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition2-isdurationknown">IsDurationKnown</a>
</td>
<td align="left" width="63%">
Determines whether the duration of a transition is known.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition2-setinitialvalue">SetInitialValue</a>
</td>
<td align="left" width="63%">
Sets the initial value of the transition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition2-setinitialvectorvalue">SetInitialVectorValue</a>
</td>
<td align="left" width="63%">
Sets the initial value of the transition for each specified dimension in the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition2-setinitialvectorvelocity">SetInitialVectorVelocity</a>
</td>
<td align="left" width="63%">
Sets the initial velocity of the transition for each specified dimension in the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationtransition2-setinitialvelocity">SetInitialVelocity</a>
</td>
<td align="left" width="63%">
Sets the initial velocity of the transition.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/UIAnimation/-interfaces-main">Interfaces</a>

