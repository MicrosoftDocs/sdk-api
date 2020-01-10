---
UID: NN:mileffects.IMILBitmapEffectPrimitive
title: IMILBitmapEffectPrimitive (mileffects.h)
description: Exposes methods that create a bitmap effect's output. This interface must be implemented to create third party Windows Presentation Foundation (WPF) bitmap effects.
old-location: wibe\_wibe_imilbitmapeffectprimitive.htm
tech.root: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectprimitive\imilbitmapeffectprimitive.htm
ms.date: 12/05/2018
ms.keywords: IMILBitmapEffectPrimitive, IMILBitmapEffectPrimitive interface [WPF Bitmap Effects], IMILBitmapEffectPrimitive interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectprimitive, mileffects/IMILBitmapEffectPrimitive, wibe._wibe_imilbitmapeffectprimitive
f1_keywords:
- mileffects/IMILBitmapEffectPrimitive
dev_langs:
- c++
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
req.lib: 
req.dll: Mileffects.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mileffects.dll
api_name:
- IMILBitmapEffectPrimitive
targetos: Windows
req.typenames: 
req.redist: Microsoft .Net 3.0
ms.custom: 19H1
---

# IMILBitmapEffectPrimitive interface


## -description


Exposes methods that create a bitmap effect's output. This interface must be implemented to create third party Windows Presentation Foundation (WPF) bitmap effects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMILBitmapEffectPrimitive</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMILBitmapEffectPrimitive</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectprimitive-getaffinematrix">GetAffineMatrix</a>
</td>
<td align="left" width="63%">
Retrieves the affine transormation matrix for the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectprimitive-getoutput">GetOutput</a>
</td>
<td align="left" width="63%">
Performs pixel processing for the bitmap effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectprimitive-hasaffinetransform">HasAffineTransform</a>
</td>
<td align="left" width="63%">
Determines whether the effect has an affine transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectprimitive-hasinversetransform">HasInverseTransform</a>
</td>
<td align="left" width="63%">
Determines whether the effect has an inverse transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectprimitive-transformpoint">TransformPoint</a>
</td>
<td align="left" width="63%">
Transforms the given point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nf-mileffects-imilbitmapeffectprimitive-transformrect">TransformRect</a>
</td>
<td align="left" width="63%">
Transforms the output of the given rectangle.

</td>
</tr>
</table> 


## -remarks



Effect clients, in general, should interact with the outer <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffect">IMILBitmapEffect</a> object rather than the <b>IMILBitmapEffectPrimitive</b> object.
            If the client needs to interact with the <b>IMILBitmapEffectPrimitive</b> directly the client will need to implement <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectconnections">IMILBitmapEffectConnections</a>, <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectconnectionsinfo">IMILBitmapEffectConnectionsInfo</a>, and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mileffects/nn-mileffects-imilbitmapeffectconnectorinfo">IMILBitmapEffectConnectorInfo</a>.
         



