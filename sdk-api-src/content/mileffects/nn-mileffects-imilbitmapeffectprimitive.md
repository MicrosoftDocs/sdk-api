---
UID: NN:mileffects.IMILBitmapEffectPrimitive
title: IMILBitmapEffectPrimitive
author: windows-sdk-content
description: Exposes methods that create a bitmap effect's output. This interface must be implemented to create third party Windows Presentation Foundation (WPF) bitmap effects.
old-location: wibe\_wibe_imilbitmapeffectprimitive.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectprimitive\imilbitmapeffectprimitive.htm
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: IMILBitmapEffectPrimitive, IMILBitmapEffectPrimitive interface [WPF Bitmap Effects], IMILBitmapEffectPrimitive interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectprimitive, mileffects/IMILBitmapEffectPrimitive, wibe._wibe_imilbitmapeffectprimitive
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mileffects.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mileffects.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MICUIELEMENTSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mileffects.dll
api_name:
 - IMILBitmapEffectPrimitive
product: Windows
targetos: Windows
req.lib: 
req.dll: Mileffects.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMILBitmapEffectPrimitive interface


## -description


Exposes methods that create a bitmap effect's output. This interface must be implemented to create third party Windows Presentation Foundation (WPF) bitmap effects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectPrimitive</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMILBitmapEffectPrimitive</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMILBitmapEffectPrimitive</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms735254(v=VS.85).aspx">GetAffineMatrix</a>
</td>
<td align="left" width="63%">
Retrieves the affine transormation matrix for the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms735255(v=VS.85).aspx">GetOutput</a>
</td>
<td align="left" width="63%">
Performs pixel processing for the bitmap effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms735256(v=VS.85).aspx">HasAffineTransform</a>
</td>
<td align="left" width="63%">
Determines whether the effect has an affine transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms735257(v=VS.85).aspx">HasInverseTransform</a>
</td>
<td align="left" width="63%">
Determines whether the effect has an inverse transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms735259(v=VS.85).aspx">TransformPoint</a>
</td>
<td align="left" width="63%">
Transforms the given point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/ms735260(v=VS.85).aspx">TransformRect</a>
</td>
<td align="left" width="63%">
Transforms the output of the given rectangle.

</td>
</tr>
</table> 


## -remarks




            Effect clients, in general, should interact with the outer <a href="https://msdn.microsoft.com/library/ms735317(v=VS.85).aspx">IMILBitmapEffect</a> object rather than the <b>IMILBitmapEffectPrimitive</b> object.
            If the client needs to interact with the <b>IMILBitmapEffectPrimitive</b> directly the client will need to implement <a href="https://msdn.microsoft.com/library/ms735314(v=VS.85).aspx">IMILBitmapEffectConnections</a>, <a href="https://msdn.microsoft.com/library/ms735311(v=VS.85).aspx">IMILBitmapEffectConnectionsInfo</a>, and <a href="https://msdn.microsoft.com/library/ms735303(v=VS.85).aspx">IMILBitmapEffectConnectorInfo</a>.
         



