---
UID: NN:d2d1svg.ID2D1SvgDocument
title: ID2D1SvgDocument
author: windows-sdk-content
description: Represents an SVG document.
old-location: direct2d\id2d1svgdocument.htm
tech.root: direct2d
ms.assetid: 1F570A77-7110-4C71-A7BE-74F2B78CFE96
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: ID2D1SvgDocument, ID2D1SvgDocument interface [Direct2D], ID2D1SvgDocument interface [Direct2D],described, d2d1svg/ID2D1SvgDocument, direct2d.id2d1svgdocument
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - direct2d.dll
api_name:
 - ID2D1SvgDocument
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SvgDocument interface


## -description


Represents an SVG document.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1SvgDocument</b> interface inherits from <a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>. <b>ID2D1SvgDocument</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/dba9be4a-1670-7ab9-e0a8-d9f2895011f4">CreatePaint</a>
</td>
<td align="left" width="63%">Overloaded. Creates a paint object which can be used to set the 'fill' or 'stroke' properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3BF28252-AC33-4B16-9A72-2838006C4A21">CreatePathData</a>
</td>
<td align="left" width="63%">
Creates a path data object which can be used to set a 'd' attribute on a 'path' element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A7AB02F2-32B0-4FF5-8A3A-CE7A6AD9DB57">CreatePointCollection</a>
</td>
<td align="left" width="63%">
Creates a points object which can be used to set a points attribute on a polygon or polyline element.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/559330E4-A0B9-437A-AD83-02C9409B5BE2">CreateStrokeDashArray</a>
</td>
<td align="left" width="63%">
Creates a dash array object which can be used to set the stroke-dasharray property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/576A1D80-3FB5-4495-85CD-2E1DDBCA1C99">Deserialize</a>
</td>
<td align="left" width="63%">
Deserializes a subtree from the stream. The stream must have only one root element, but that root element need not be an 'svg' element.
          The output element is not inserted into this document tree.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B4E4EE0E-0A2B-479A-B101-AC9DF8546A4F">FindElementById</a>
</td>
<td align="left" width="63%">
Gets the SVG element with the specified ID. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01E11639-7564-41F4-BFA4-28B05FC50583">GetRoot</a>
</td>
<td align="left" width="63%">
Gets the root element of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3CE19841-86BD-4122-B2B0-F4F3A530523D">GetViewportSize</a>
</td>
<td align="left" width="63%">
Returns the size of the initial viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/799E975A-F3BF-4832-AE51-DA064E5C698E">Serialize</a>
</td>
<td align="left" width="63%">
Serializes an element and its subtree to XML. The output XML is encoded as UTF-8.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/076DC8F7-E358-484D-A567-60E80F9D2FC3">SetRoot</a>
</td>
<td align="left" width="63%">
Sets the root element of the document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2915630B-A76B-40E7-8586-B0B0EFD30780">SetViewportSize</a>
</td>
<td align="left" width="63%">
Sets the size of the initial viewport.

</td>
</tr>
</table> 

