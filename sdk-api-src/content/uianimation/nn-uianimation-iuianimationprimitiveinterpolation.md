---
UID: NN:uianimation.IUIAnimationPrimitiveInterpolation
title: IUIAnimationPrimitiveInterpolation (uianimation.h)
author: windows-sdk-content
description: Defines a method that allows a custom interpolator to provide transition information, in the form of a cubic polynomial curve, to the animation manager.
old-location: uianimation\iuianimationprimitiveinterpolation.htm
tech.root: UIAnimation
ms.assetid: 6EAE7874-1103-4D2E-A325-37E5A95705F5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAnimationPrimitiveInterpolation, IUIAnimationPrimitiveInterpolation interface [Windows Animation], IUIAnimationPrimitiveInterpolation interface [Windows Animation],described, uianimation.iuianimationprimitiveinterpolation, uianimation/IUIAnimationPrimitiveInterpolation
ms.topic: interface
f1_keywords: 
 - "uianimation/IUIAnimationPrimitiveInterpolation"
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
 - IUIAnimationPrimitiveInterpolation
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAnimationPrimitiveInterpolation interface


## -description


Defines a method that allows a custom interpolator to provide transition information, in the form of a cubic polynomial curve, to the animation manager.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationPrimitiveInterpolation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAnimationPrimitiveInterpolation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationPrimitiveInterpolation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nf-uianimation-iuianimationprimitiveinterpolation-addcubic">AddCubic</a>
</td>
<td align="left" width="63%">
Adds a cubic polynomial segment to the animation function.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uianimation/nn-uianimation-iuianimationinterpolator2">IUIAnimationInterpolator2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/UIAnimation/-interfaces-main">Interfaces</a>
 

 

