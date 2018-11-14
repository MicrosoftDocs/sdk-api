---
UID: NN:uianimation.IUIAnimationPrimitiveInterpolation
title: IUIAnimationPrimitiveInterpolation
author: windows-sdk-content
description: Defines a method that allows a custom interpolator to provide transition information, in the form of a cubic polynomial curve, to the animation manager.
old-location: uianimation\iuianimationprimitiveinterpolation.htm
tech.root: UIAnimation
ms.assetid: 6EAE7874-1103-4D2E-A325-37E5A95705F5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IUIAnimationPrimitiveInterpolation, IUIAnimationPrimitiveInterpolation interface [Windows Animation], IUIAnimationPrimitiveInterpolation interface [Windows Animation],described, uianimation.iuianimationprimitiveinterpolation, uianimation/IUIAnimationPrimitiveInterpolation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAnimationPrimitiveInterpolation interface


## -description


Defines a method that allows a custom interpolator to provide transition information, in the form of a cubic polynomial curve, to the animation manager.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationPrimitiveInterpolation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationPrimitiveInterpolation</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/98738F6A-364E-491F-BCA3-F8B74B036D89">AddCubic</a>
</td>
<td align="left" width="63%">
Adds a cubic polynomial segment to the animation function.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/EC0D1933-37C3-41E2-AB13-DA4AAF4B8F04">IUIAnimationInterpolator2</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/b54e319c-e140-4fd9-8045-5eb6f4a31326">Interfaces</a>
 

 

