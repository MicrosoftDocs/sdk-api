---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.SetFontFaceIndex
title: IXpsOMGlyphs::SetFontFaceIndex (xpsobjectmodel.h)
description: Sets the index of the font face to be used.
helpviewer_keywords: ["IXpsOMGlyphs interface [XPS Documents and Packaging]","SetFontFaceIndex method","IXpsOMGlyphs.SetFontFaceIndex","IXpsOMGlyphs::SetFontFaceIndex","SetFontFaceIndex","SetFontFaceIndex method [XPS Documents and Packaging]","SetFontFaceIndex method [XPS Documents and Packaging]","IXpsOMGlyphs interface","xps.ixpsomglyphs_setfontfaceindex","xpsobjectmodel/IXpsOMGlyphs::SetFontFaceIndex"]
old-location: xps\ixpsomglyphs_setfontfaceindex.htm
tech.root: printdocs
ms.assetid: 9430474d-b874-47c7-b916-089280da8873
ms.date: 12/05/2018
ms.keywords: IXpsOMGlyphs interface [XPS Documents and Packaging],SetFontFaceIndex method, IXpsOMGlyphs.SetFontFaceIndex, IXpsOMGlyphs::SetFontFaceIndex, SetFontFaceIndex, SetFontFaceIndex method [XPS Documents and Packaging], SetFontFaceIndex method [XPS Documents and Packaging],IXpsOMGlyphs interface, xps.ixpsomglyphs_setfontfaceindex, xpsobjectmodel/IXpsOMGlyphs::SetFontFaceIndex
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
 - IXpsOMGlyphs::SetFontFaceIndex
 - xpsobjectmodel/IXpsOMGlyphs::SetFontFaceIndex
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
 - IXpsOMGlyphs.SetFontFaceIndex
---

# IXpsOMGlyphs::SetFontFaceIndex


## -description

Sets the index of the font face to be used.

This value is only used when <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomglyphs-getfontresource">GetFontResource</a> returns an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a> interface that  represents a <b>TrueType</b> font collection.

## -parameters

### -param fontFaceIndex [in]

The index value of the font face to be used.

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
The value of <i>fontFaceIndex</i> is not valid; it must be an integer that is greater than or equal to –1.

</td>
</tr>
</table>

## -remarks

The default value of the font face index property is –1, which means that a font index has not been set or the font resource is not a  <b>TrueType</b> font collection.

If this value is specified and is not –1, "#&lt;Index&gt;" is appended to the Font URI during serialization. Here, &lt;Index&gt; is the value that is set by <b>SetFontFaceIndex</b>.

The following markup of a FixedPage shows the result of setting the <i>fontFaceIndex</i> to 1. Notice that the <b>FontUri</b> attribute of the <b>Glyphs</b> element has a value of <code>../Resources/Fonts/Font.TTF#1</code>, which includes the index of the font face.


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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
