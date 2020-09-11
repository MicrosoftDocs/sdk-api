---
UID: NN:d2d1svg.ID2D1SvgDocument
title: ID2D1SvgDocument (d2d1svg.h)
description: Represents an SVG document.
helpviewer_keywords: ["ID2D1SvgDocument","ID2D1SvgDocument interface [Direct2D]","ID2D1SvgDocument interface [Direct2D]","described","d2d1svg/ID2D1SvgDocument","direct2d.id2d1svgdocument"]
old-location: direct2d\id2d1svgdocument.htm
tech.root: Direct2D
ms.assetid: 1F570A77-7110-4C71-A7BE-74F2B78CFE96
ms.date: 12/05/2018
ms.keywords: ID2D1SvgDocument, ID2D1SvgDocument interface [Direct2D], ID2D1SvgDocument interface [Direct2D],described, d2d1svg/ID2D1SvgDocument, direct2d.id2d1svgdocument
req.header: d2d1svg.h
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
req.dll: Direct2d.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1SvgDocument
 - d2d1svg/ID2D1SvgDocument
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - direct2d.dll
api_name:
 - ID2D1SvgDocument
---

# ID2D1SvgDocument interface


## -description

Represents an SVG document.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SvgDocument</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1SvgDocument</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1SvgDocument</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-createpaint">CreatePaint</a>
</td>
<td align="left" width="63%">Overloaded. Creates a paint object which can be used to set the 'fill' or 'stroke' properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgdocument-createpathdata">CreatePathData</a>
</td>
<td align="left" width="63%">
Creates a path data object which can be used to set a 'd' attribute on a 'path' element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgdocument-createpointcollection">CreatePointCollection</a>
</td>
<td align="left" width="63%">
Creates a points object which can be used to set a points attribute on a polygon or polyline element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgdocument-createstrokedasharray">CreateStrokeDashArray</a>
</td>
<td align="left" width="63%">
Creates a dash array object which can be used to set the stroke-dasharray property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgdocument-deserialize">Deserialize</a>
</td>
<td align="left" width="63%">
Deserializes a subtree from the stream. The stream must have only one root element, but that root element need not be an 'svg' element.
          The output element is not inserted into this document tree.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgdocument-findelementbyid">FindElementById</a>
</td>
<td align="left" width="63%">
Gets the SVG element with the specified ID. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgdocument-getroot">GetRoot</a>
</td>
<td align="left" width="63%">
Gets the root element of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgdocument-getviewportsize">GetViewportSize</a>
</td>
<td align="left" width="63%">
Returns the size of the initial viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgdocument-serialize">Serialize</a>
</td>
<td align="left" width="63%">
Serializes an element and its subtree to XML. The output XML is encoded as UTF-8.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgdocument-setroot">SetRoot</a>
</td>
<td align="left" width="63%">
Sets the root element of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d2d1svg/nf-d2d1svg-id2d1svgdocument-setviewportsize">SetViewportSize</a>
</td>
<td align="left" width="63%">
Sets the size of the initial viewport.

</td>
</tr>
</table>

