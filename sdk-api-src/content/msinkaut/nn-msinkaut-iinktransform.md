---
UID: NN:msinkaut.IInkTransform
title: IInkTransform (msinkaut.h)

description: "."
old-location: tablet\iinktransform.htm
tech.root: tablet
ms.assetid: 1C9562EF-8CF4-4F0C-94FC-3ED54F6493E5

ms.date: 12/05/2018
ms.keywords: IInkTransform, IInkTransform interface [Tablet PC], IInkTransform interface [Tablet PC],described, msinkaut/IInkTransform, tablet.iinktransform
ms.topic: interface
f1_keywords: 
 - "msinkaut/IInkTransform"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msinkaut.h
api_name:
 - IInkTransform
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkTransform interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkTransform</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkTransform</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-gettransform">GetTransform</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/tablet/inktransform-class">InkTransform</a> member data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reflect">Reflect</a>
</td>
<td align="left" width="63%">
Performs reflection on a transform in either horizontal or vertical directions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the transform to its default state, the identity transform.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-rotate">Rotate</a>
</td>
<td align="left" width="63%">
Changes the amount, measured in degrees, to change the rotation factor of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inktransform-class">InkTransform</a> object and optionally the center point of the rotation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-scaletransform">ScaleTransform</a>
</td>
<td align="left" width="63%">
Applies the specified horizontal and vertical factors to the transform or ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-settransform">SetTransform</a>
</td>
<td align="left" width="63%">
Modifies the <a href="https://docs.microsoft.com/windows/desktop/tablet/inktransform-class">InkTransform</a> member data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-shear">Shear</a>
</td>
<td align="left" width="63%">
Adjusts the shear of the <a href="https://docs.microsoft.com/windows/desktop/tablet/inktransform-class">InkTransform</a> by the specified horizontal and vertical factors.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-translate">Translate</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_data">Data</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edx">eDx</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the element in the third row, first column of the affine transform matrix that is represented by an <a href="https://docs.microsoft.com/windows/desktop/tablet/inktransform-class">InkTransform</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_edy">eDy</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the element in the third row, second column of the affine transform matrix that is represented by an <a href="https://docs.microsoft.com/windows/desktop/tablet/inktransform-class">InkTransform</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em11">eM11</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the element in the first row, first column of the affine transform matrix that is represented by an <a href="https://docs.microsoft.com/windows/desktop/tablet/inktransform-class">InkTransform</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em12">eM12</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the element in the first row, second column of the affine transform matrix that is represented by an <a href="https://docs.microsoft.com/windows/desktop/tablet/inktransform-class">InkTransform</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em21">eM21</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the element in the second row, first column of the affine transform matrix that is represented by an <a href="https://docs.microsoft.com/windows/desktop/tablet/inktransform-class">InkTransform</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinktransform-get_em22">eM22</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the element in the second row, second column of the affine transform matrix that is represented by an <a href="https://docs.microsoft.com/windows/desktop/tablet/inktransform-class">InkTransform</a> object.

</td>
</tr>
</table> 

