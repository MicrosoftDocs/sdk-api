---
UID: NN:uianimation.IUIAnimationVariable2
title: IUIAnimationVariable2 (uianimation.h)
description: Defines an animation variable, which represents a visual element that can be animated in multiple dimensions.
old-location: uianimation\iuianimationvariable2.htm
tech.root: UIAnimation
ms.assetid: A676EF27-B59D-4D2D-AD5B-8F46EE337E69
ms.date: 12/05/2018
ms.keywords: IUIAnimationVariable2, IUIAnimationVariable2 interface [Windows Animation], IUIAnimationVariable2 interface [Windows Animation],described, uianimation.iuianimationvariable2, uianimation/IUIAnimationVariable2
f1_keywords:
- uianimation/IUIAnimationVariable2
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
- IUIAnimationVariable2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationVariable2 interface


## -description


Defines an animation variable, which represents a visual element that can be animated in multiple dimensions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationVariable2</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationVariable2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationVariable2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getcurrentstoryboard">GetCurrentStoryboard</a>
</td>
<td align="left" width="63%">
Gets the active storyboard for the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getcurve">GetCurve</a>
</td>
<td align="left" width="63%">
Gets the animation curve of the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getdimension">GetDimension</a>
</td>
<td align="left" width="63%">
Gets the number of dimensions that the animation variable is to be animated in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getfinalintegervalue">GetFinalIntegerValue</a>
</td>
<td align="left" width="63%">
Gets the final integer value of the animation variable. This is the value after all currently scheduled animations have completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getfinalintegervectorvalue">GetFinalIntegerVectorValue</a>
</td>
<td align="left" width="63%">
Gets the final integer value of the animation variable for the specified dimension. This is the value after all currently scheduled animations have completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getfinalvalue">GetFinalValue</a>
</td>
<td align="left" width="63%">
Gets the final value of the animation variable. This is the value after all currently scheduled animations have completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getfinalvectorvalue">GetFinalVectorValue</a>
</td>
<td align="left" width="63%">
Gets the final value of the animation variable for the specified dimension. This is the value after all currently scheduled animations have completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getintegervalue">GetIntegerValue</a>
</td>
<td align="left" width="63%">
Gets the integer value of the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getintegervectorvalue">GetIntegerVectorValue</a>
</td>
<td align="left" width="63%">
Gets the integer value of the animation variable for the specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getpreviousintegervalue">GetPreviousIntegerValue</a>
</td>
<td align="left" width="63%">
Gets the previous integer value of the animation variable in the specified dimension. This is the value of the animation variable before the most recent update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getpreviousintegervectorvalue">GetPreviousIntegerVectorValue</a>
</td>
<td align="left" width="63%">
Gets the previous integer value of the animation variable for the specified dimension. This is the value of the animation variable before the most recent update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getpreviousvalue">GetPreviousValue</a>
</td>
<td align="left" width="63%">
Gets the previous value of the animation variable. This is the value of the animation variable before the most recent update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getpreviousvectorvalue">GetPreviousVectorValue</a>
</td>
<td align="left" width="63%">
Gets the previous value of the animation variable for the specified dimension. This is the value of the animation variable before the most recent update.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-gettag">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag of the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Gets the value of the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getvectorcurve">GetVectorCurve</a>
</td>
<td align="left" width="63%">
Gets the animation curve of the animation variable for the specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-getvectorvalue">GetVectorValue</a>
</td>
<td align="left" width="63%">
Gets the value of the animation variable in the specified dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-setlowerbound">SetLowerBound</a>
</td>
<td align="left" width="63%">
Sets the lower bound (floor) for the value of the animation variable. The value of the animation variable should not fall below the specified value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-setlowerboundvector">SetLowerBoundVector</a>
</td>
<td align="left" width="63%">
Sets the lower bound (floor) value of each specified dimension for the animation variable. The value of each animation variable should not fall below its lower bound.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-setroundingmode">SetRoundingMode</a>
</td>
<td align="left" width="63%">
Sets the rounding mode of the animation variable.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-settag">SetTag</a>
</td>
<td align="left" width="63%">
Sets the tag of the animation variable.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-setupperbound">SetUpperBound</a>
</td>
<td align="left" width="63%">
Sets the upper bound (ceiling) for the value of the animation variable. The value of the animation variable should not rise above the specified value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-setupperboundvector">SetUpperBoundVector</a>
</td>
<td align="left" width="63%">
Sets the upper bound (ceiling) value of each specified dimension for the animation variable. The value of each animation variable should not rise above its upper bound.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-setvariablechangehandler">SetVariableChangeHandler</a>
</td>
<td align="left" width="63%">
Specifies a handler for changes to the value of the animation variable. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-setvariablecurvechangehandler">SetVariableCurveChangeHandler</a>
</td>
<td align="left" width="63%">
Specifies a handler for changes to the animation curve of the animation variable. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationvariable2-setvariableintegerchangehandler">SetVariableIntegerChangeHandler</a>
</td>
<td align="left" width="63%">
Specifies a handler for changes to the integer value of the animation variable. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/UIAnimation/-interfaces-main">Interfaces</a>
 

 

