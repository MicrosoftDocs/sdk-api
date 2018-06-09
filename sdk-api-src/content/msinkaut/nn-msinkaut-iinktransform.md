---
UID: NN:msinkaut.IInkTransform
title: IInkTransform
author: windows-sdk-content
description: "."
old-location: tablet\iinktransform.htm
old-project: tablet
ms.assetid: 1C9562EF-8CF4-4F0C-94FC-3ED54F6493E5
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IInkTransform, IInkTransform interface [Tablet PC], IInkTransform interface [Tablet PC],described, msinkaut/IInkTransform, tablet.iinktransform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msinkaut.h
api_name:
 - IInkTransform
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkTransform interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkTransform</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInkTransform</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkTransform</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d6aec579-7fa4-4cfb-8f63-2810b0c40103">GetTransform</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> member data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebecd285-4dc4-4f4a-9d07-a3287b0438e9">Reflect</a>
</td>
<td align="left" width="63%">
Performs reflection on a transform in either horizontal or vertical directions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the transform to its default state, the identity transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17d7e4b0-ccde-4ad9-9bdc-0f6a72ee762e">Rotate</a>
</td>
<td align="left" width="63%">
Changes the amount, measured in degrees, to change the rotation factor of the <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object and optionally the center point of the rotation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49da109e-afca-4695-94ab-e4ed00d82e5a">ScaleTransform</a>
</td>
<td align="left" width="63%">
Applies the specified horizontal and vertical factors to the transform or ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b734703-4117-4668-b881-4ba4e1c65189">SetTransform</a>
</td>
<td align="left" width="63%">
Modifies the <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> member data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a3d828e-33cc-435f-9276-7c3304cca71d">Shear</a>
</td>
<td align="left" width="63%">
Adjusts the shear of the <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> by the specified horizontal and vertical factors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3125e27b-a280-43bc-99d7-a6b5697366b2">Translate</a>
</td>
<td align="left" width="63%">
Applies a translation to a transform.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkTransform</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/mt427307">Data</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets access to the <a href="http://go.microsoft.com/fwlink/p/?linkid=9696">XFORM structure</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f2e6fabc-4a8a-4225-b518-438e1d0ca196">eDx</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the element in the third row, first column of the affine transform matrix that is represented by an <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d7f35091-93c0-45aa-87e4-49abf89998e5">eDy</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the element in the third row, second column of the affine transform matrix that is represented by an <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8827b2b2-f2fb-4732-912c-226db8ac9aef">eM11</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the element in the first row, first column of the affine transform matrix that is represented by an <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e0cfcd30-49b7-457f-8e1f-faa433b4e8ef">eM12</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the element in the first row, second column of the affine transform matrix that is represented by an <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/66fd4f89-7e50-4594-9010-54baed20f2e6">eM21</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the element in the second row, first column of the affine transform matrix that is represented by an <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/46a50a77-f834-4d75-89db-a9be6e1ed24f">eM22</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the element in the second row, second column of the affine transform matrix that is represented by an <a href="https://msdn.microsoft.com/79abff2e-d1d3-4a32-9ac2-f46c1b21f742">InkTransform</a> object.

</td>
</tr>
</table> 

