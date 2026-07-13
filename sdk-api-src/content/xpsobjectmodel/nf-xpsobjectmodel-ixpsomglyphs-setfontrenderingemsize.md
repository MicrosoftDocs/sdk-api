---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.SetFontRenderingEmSize
title: IXpsOMGlyphs::SetFontRenderingEmSize (xpsobjectmodel.h)
description: Sets the font size of the text.
helpviewer_keywords: ["IXpsOMGlyphs interface [XPS Documents and Packaging]","SetFontRenderingEmSize method","IXpsOMGlyphs.SetFontRenderingEmSize","IXpsOMGlyphs::SetFontRenderingEmSize","SetFontRenderingEmSize","SetFontRenderingEmSize method [XPS Documents and Packaging]","SetFontRenderingEmSize method [XPS Documents and Packaging]","IXpsOMGlyphs interface","xps.ixpsomglyphs_setfontrenderingemsize","xpsobjectmodel/IXpsOMGlyphs::SetFontRenderingEmSize"]
old-location: xps\ixpsomglyphs_setfontrenderingemsize.htm
tech.root: xps
ms.assetid: 9863caa0-9f43-45f7-9bed-c5b7187491de
ms.date: 12/05/2018
ms.keywords: IXpsOMGlyphs interface [XPS Documents and Packaging],SetFontRenderingEmSize method, IXpsOMGlyphs.SetFontRenderingEmSize, IXpsOMGlyphs::SetFontRenderingEmSize, SetFontRenderingEmSize, SetFontRenderingEmSize method [XPS Documents and Packaging], SetFontRenderingEmSize method [XPS Documents and Packaging],IXpsOMGlyphs interface, xps.ixpsomglyphs_setfontrenderingemsize, xpsobjectmodel/IXpsOMGlyphs::SetFontRenderingEmSize
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
 - IXpsOMGlyphs::SetFontRenderingEmSize
 - xpsobjectmodel/IXpsOMGlyphs::SetFontRenderingEmSize
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
 - IXpsOMGlyphs.SetFontRenderingEmSize
---

# IXpsOMGlyphs::SetFontRenderingEmSize


## -description

Sets the font size of the text.

## -parameters

### -param fontRenderingEmSize [in]

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>fontRenderingEmSize</i> is not valid; it must be a non-negative number.

</td>
</tr>
</table>

## -remarks

The em size returned in <i>fontRenderingEmSize</i> specifies the font size in  drawing surface units. Drawing surface units are expressed as floating-point values in the units of the effective coordinate space.

In new glyph objects, the default value of <i>fontRenderingEmSize</i> is 10.0.

If the value of <i>fontRenderingEmSize</i> is 0.0, no text is displayed.

A value of 0.0 results in no visible text being displayed.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>