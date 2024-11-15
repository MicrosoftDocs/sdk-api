---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetFontFaceIndex
title: IXpsOMGlyphs::GetFontFaceIndex (xpsobjectmodel.h)
description: Gets the index of the font face to be used.
helpviewer_keywords: ["GetFontFaceIndex","GetFontFaceIndex method [XPS Documents and Packaging]","GetFontFaceIndex method [XPS Documents and Packaging]","IXpsOMGlyphs interface","IXpsOMGlyphs interface [XPS Documents and Packaging]","GetFontFaceIndex method","IXpsOMGlyphs.GetFontFaceIndex","IXpsOMGlyphs::GetFontFaceIndex","xps.ixpsomglyphs_getfontfaceindex","xpsobjectmodel/IXpsOMGlyphs::GetFontFaceIndex"]
old-location: xps\ixpsomglyphs_getfontfaceindex.htm
tech.root: printdocs
ms.assetid: 375e6391-c75f-4dbe-b51f-ce394f5088ec
ms.date: 12/05/2018
ms.keywords: GetFontFaceIndex, GetFontFaceIndex method [XPS Documents and Packaging], GetFontFaceIndex method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetFontFaceIndex method, IXpsOMGlyphs.GetFontFaceIndex, IXpsOMGlyphs::GetFontFaceIndex, xps.ixpsomglyphs_getfontfaceindex, xpsobjectmodel/IXpsOMGlyphs::GetFontFaceIndex
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
 - IXpsOMGlyphs::GetFontFaceIndex
 - xpsobjectmodel/IXpsOMGlyphs::GetFontFaceIndex
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
 - IXpsOMGlyphs.GetFontFaceIndex
---

# IXpsOMGlyphs::GetFontFaceIndex


## -description

Gets the index of the font face to be used.

This value is only used when <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-getfontresource">GetFontResource</a> returns an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a> interface that  represents a <b>TrueType</b> font collection.

## -parameters

### -param fontFaceIndex [out, retval]

The index value of the font face. If the font face has not been set, –1 is returned.

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
<i>fontFaceIndex</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The font resource is obtained by calling the <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-getfontresource">GetFontResource</a> method.

If a font face has not been set or is not supported by the font, a value of –1 is returned in <i>fontFaceIndex</i>. When the glyph is loaded from an existing XPS document file, a <i>fontFaceIndex</i> value of –1 indicates that the <b>FontUri</b> attribute did not include a <b>#index</b> fragment.

In the following markup of a FixedPage, the <b>FontUri</b> attribute of the <b>Glyphs</b> element has a value of <code>../Resources/Fonts/Font.TTF#1</code>. In this case, <b>GetFontFaceIndex</b>  would return a value of 1 in <i>fontFaceIndex</i>.


``` syntax
    <FixedPage Height="1056" Width="816" xml:lang="en-US"
    xmlns="http://schemas.microsoft.com/xps/2005/06">
      <Glyphs
      OriginX="96"
      OriginY="96"
      UnicodeString="This is Page 1!"
      FontUri="../Resources/Fonts/Font.TTF#1"
      FontRenderingEmSize="16" />
    </FixedPage>
```


## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-getfontresource">GetFontResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
