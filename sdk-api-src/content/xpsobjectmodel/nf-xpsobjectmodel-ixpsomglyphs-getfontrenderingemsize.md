---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetFontRenderingEmSize
title: IXpsOMGlyphs::GetFontRenderingEmSize (xpsobjectmodel.h)
description: Gets the font size. (IXpsOMGlyphs.GetFontRenderingEmSize)
helpviewer_keywords: ["GetFontRenderingEmSize","GetFontRenderingEmSize method [XPS Documents and Packaging]","GetFontRenderingEmSize method [XPS Documents and Packaging]","IXpsOMGlyphs interface","IXpsOMGlyphs interface [XPS Documents and Packaging]","GetFontRenderingEmSize method","IXpsOMGlyphs.GetFontRenderingEmSize","IXpsOMGlyphs::GetFontRenderingEmSize","xps.ixpsomglyphs_getfontrenderingemsize","xpsobjectmodel/IXpsOMGlyphs::GetFontRenderingEmSize"]
old-location: xps\ixpsomglyphs_getfontrenderingemsize.htm
tech.root: xps
ms.assetid: be1c6eff-20ef-49d3-929e-3595b421bcb9
ms.date: 12/05/2018
ms.keywords: GetFontRenderingEmSize, GetFontRenderingEmSize method [XPS Documents and Packaging], GetFontRenderingEmSize method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetFontRenderingEmSize method, IXpsOMGlyphs.GetFontRenderingEmSize, IXpsOMGlyphs::GetFontRenderingEmSize, xps.ixpsomglyphs_getfontrenderingemsize, xpsobjectmodel/IXpsOMGlyphs::GetFontRenderingEmSize
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMGlyphs::GetFontRenderingEmSize
 - xpsobjectmodel/IXpsOMGlyphs::GetFontRenderingEmSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMGlyphs.GetFontRenderingEmSize
---

# IXpsOMGlyphs::GetFontRenderingEmSize


## -description

Gets the font size.

## -parameters

### -param fontRenderingEmSize [out, retval]

The  font size.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>fontRenderingEmSize</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The em size that is returned in <i>fontRenderingEmSize</i> specifies the font size in the drawing surface units. The drawing surface units are expressed as floating-point values in the effective coordinate space.

In new glyph objects, the default value of <i>fontRenderingEmSize</i> is 10.0.

If the value of <i>fontRenderingEmSize</i> is 0.0, no text is displayed.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
