---
UID: NN:mileffects.IMILBitmapEffectPrimitive
title: IMILBitmapEffectPrimitive
author: windows-driver-content
description: Exposes methods that create a bitmap effect's output. This interface must be implemented to create third party Windows Presentation Foundation (WPF) bitmap effects.
old-location: wibe\_wibe_imilbitmapeffectprimitive.htm
old-project: wibe
ms.assetid: VS|wibe|~\wibelh\reference\ifaces\imilbitmapeffectprimitive\imilbitmapeffectprimitive.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IMILBitmapEffectPrimitive, IMILBitmapEffectPrimitive interface [WPF Bitmap Effects], IMILBitmapEffectPrimitive interface [WPF Bitmap Effects],described, _wibe_imilbitmapeffectprimitive, mileffects/IMILBitmapEffectPrimitive, wibe._wibe_imilbitmapeffectprimitive
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MICUIELEMENTSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mileffects.dll
api_name:
-	IMILBitmapEffectPrimitive
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
<a href="https://msdn.microsoft.com/b6cf0c16-eb52-4d82-a2b4-769116269637">GetAffineMatrix</a>
</td>
<td align="left" width="63%">
Retrieves the affine transormation matrix for the effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8aa606e2-710a-4621-9311-7e0daaad7ef1">GetOutput</a>
</td>
<td align="left" width="63%">
Performs pixel processing for the bitmap effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4851584e-47f3-42f6-ab80-fc82d0cb64ed">HasAffineTransform</a>
</td>
<td align="left" width="63%">
Determines whether the effect has an affine transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80904f52-8f1e-4f53-a150-78ce98455011">HasInverseTransform</a>
</td>
<td align="left" width="63%">
Determines whether the effect has an inverse transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/227e9b39-96c7-4c88-8c17-a538cd276ec2">TransformPoint</a>
</td>
<td align="left" width="63%">
Transforms the given point.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/684e619d-6047-4216-90f9-b9f6f8f7a1c8">TransformRect</a>
</td>
<td align="left" width="63%">
Transforms the output of the given rectangle.

</td>
</tr>
</table> 


## -remarks




            Effect clients, in general, should interact with the outer <a href="https://msdn.microsoft.com/74078eaa-ae95-4b9b-993b-efbfb18a164d">IMILBitmapEffect</a> object rather than the <b>IMILBitmapEffectPrimitive</b> object.
            If the client needs to interact with the <b>IMILBitmapEffectPrimitive</b> directly the client will need to implement <a href="https://msdn.microsoft.com/befa56bb-149e-4a90-a1cb-9e61e7f5366c">IMILBitmapEffectConnections</a>, <a href="https://msdn.microsoft.com/5c1eb02e-7ba9-4197-b6df-53ec84c11c14">IMILBitmapEffectConnectionsInfo</a>, and <a href="https://msdn.microsoft.com/18f9260d-b7cd-4b45-a7bd-f3bd3647eebe">IMILBitmapEffectConnectorInfo</a>.
         



