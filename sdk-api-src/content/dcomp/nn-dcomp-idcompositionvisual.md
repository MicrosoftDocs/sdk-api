---
UID: NN:dcomp.IDCompositionVisual
title: IDCompositionVisual
author: windows-sdk-content
description: Represents a Microsoft DirectComposition visual.
old-location: directcomp\idcompositionvisual.htm
tech.root: directcomp
ms.assetid: 462dfc20-ad5a-425c-94b5-f21ab05f5af8
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IDCompositionVisual, IDCompositionVisual interface [DirectComposition], IDCompositionVisual interface [DirectComposition],described, dcomp/IDCompositionVisual, directcomp.idcompositionvisual
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionVisual
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionVisual interface


## -description


Represents a Microsoft DirectComposition visual. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionVisual</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDCompositionVisual</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionVisual</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1124df5-7795-49c3-a640-f218cfdd4f1d">AddVisual</a>
</td>
<td align="left" width="63%">
Adds a new child visual to the children list of this visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3872d6a-f3f8-4343-b01d-6db5490abb13">RemoveAllVisuals</a>
</td>
<td align="left" width="63%">
Removes all visuals from the children list of this visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d77161b1-cb35-40a7-a51c-4b44ea320e78">RemoveVisual</a>
</td>
<td align="left" width="63%">
Removes a child visual from the children list of this visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F45A3619-556B-4D2C-BCB0-8D55A1397579">SetBitmapInterpolationMode</a>
</td>
<td align="left" width="63%">
Sets the BitmapInterpolationMode property, which specifies the mode for DirectComposition to use when interpolating pixels from bitmaps that are not axis-aligned or drawn exactly at scale. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88C77869-B08D-43F6-8A1E-A112743C0404">SetBorderMode</a>
</td>
<td align="left" width="63%">
Sets the BorderMode property, which specifies how to compose the edges of bitmaps and clips associated with this visual, or with visuals in the subtree rooted at this visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ACEBA4F9-E1B0-459B-8DC2-272A822AB214">SetClip</a>
</td>
<td align="left" width="63%">Overloaded. Sets the Clip property of this visual to the specified rectangular region or clip object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2F8C7930-6BBC-4CA9-86C0-168BF0F9C0BD">SetCompositeMode</a>
</td>
<td align="left" width="63%">
Sets the blending mode for this visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/894E6E30-6C28-476D-9AE5-D0664A69E03C">SetContent</a>
</td>
<td align="left" width="63%">
Sets the Content property of this visual to the specified bitmap or window wrapper.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CCA785F6-869C-460A-AF54-573BDE798685">SetEffect</a>
</td>
<td align="left" width="63%">
Sets the Effect property of this visual.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0EFCDE12-3BF1-4D1F-8E28-54F3D7EEFFC1">SetOffsetX</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the OffsetX property of this visual, altering the horizontal position of the visual relative to its parent. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E364BDB4-57E0-4206-9095-F39E6B5B9190">SetOffsetY</a>
</td>
<td align="left" width="63%">Overloaded. Changes or animates the value of the OffsetY property of this visual, altering the vertical position of the visual relative to its parent.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D">SetTransform</a>
</td>
<td align="left" width="63%">Overloaded. Sets the Transform property of this visual. The Transform  property specifies a 2D transform used to modify the coordinate system of this visual. The property can specify either a  3-by-2 transform matrix or a transform object.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06C02E3D-27FF-4E11-87C2-7D8281A69601">SetTransformParent</a>
</td>
<td align="left" width="63%">
Sets the TransformParent property of this visual. The TransformParent property establishes the coordinate system relative to which this visual is composed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3b4fefe0-772e-42bd-8e81-37d0b128c418">IDCompositionDevice::CreateVisual</a>
 

 

