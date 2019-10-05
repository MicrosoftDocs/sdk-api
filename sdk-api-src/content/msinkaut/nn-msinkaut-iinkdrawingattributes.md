---
UID: NN:msinkaut.IInkDrawingAttributes
title: IInkDrawingAttributes (msinkaut.h)
author: windows-sdk-content
description: "."
old-location: tablet\iinkdrawingattributes.htm
tech.root: tablet
ms.assetid: 47106C55-FA03-4996-BCFA-D00A51AF55EE
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IInkDrawingAttributes, IInkDrawingAttributes interface [Tablet PC], IInkDrawingAttributes interface [Tablet PC],described, msinkaut/IInkDrawingAttributes, tablet.iinkdrawingattributes
ms.topic: interface
f1_keywords: 
 - "msinkaut/IInkDrawingAttributes"
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
 - IInkDrawingAttributes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkDrawingAttributes interface


## -description





## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDrawingAttributes</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkDrawingAttributes</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IInkDrawingAttributes</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a duplicate <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInkDrawingAttributes</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_antialiased">AntiAliased</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the value that indicates whether a stroke is antialiased.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color">Color</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the color of the ink that is drawn with this <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_extendedproperties">ExtendedProperties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the collection of application-defined data that are stored in an object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve">FitToCurve</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the value that specifies whether Bezier smoothing is used to render ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height">Height</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the height of the pen when drawing ink with the <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_ignorepressure">IgnorePressure</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the value that specifies whether drawn ink automatically gets wider with increased pressure of the pen tip on the tablet surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip">PenTip</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that indicates which pen tip to use when drawing ink that is associated with this <a href="https://docs.microsoft.com/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttributes</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation">RasterOperation</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that defines how the colors of the pen and background interact.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_transparency">Transparency</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a value that indicates the transparency value of ink.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width">Width</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets the y-axis dimension, or width, of the pen tip when drawing ink.

</td>
</tr>
</table> 

