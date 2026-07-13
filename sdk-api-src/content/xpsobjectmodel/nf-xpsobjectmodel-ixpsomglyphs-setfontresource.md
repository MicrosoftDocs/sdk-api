---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.SetFontResource
title: IXpsOMGlyphs::SetFontResource (xpsobjectmodel.h)
description: Sets the pointer to the IXpsOMFontResource interface of the font resource object that is required for this text.
helpviewer_keywords: ["IXpsOMGlyphs interface [XPS Documents and Packaging]","SetFontResource method","IXpsOMGlyphs.SetFontResource","IXpsOMGlyphs::SetFontResource","SetFontResource","SetFontResource method [XPS Documents and Packaging]","SetFontResource method [XPS Documents and Packaging]","IXpsOMGlyphs interface","xps.ixpsomglyphs_setfontresource","xpsobjectmodel/IXpsOMGlyphs::SetFontResource"]
old-location: xps\ixpsomglyphs_setfontresource.htm
tech.root: xps
ms.assetid: 0de80249-a1e1-4205-81bd-3ecb6cc938d4
ms.date: 12/05/2018
ms.keywords: IXpsOMGlyphs interface [XPS Documents and Packaging],SetFontResource method, IXpsOMGlyphs.SetFontResource, IXpsOMGlyphs::SetFontResource, SetFontResource, SetFontResource method [XPS Documents and Packaging], SetFontResource method [XPS Documents and Packaging],IXpsOMGlyphs interface, xps.ixpsomglyphs_setfontresource, xpsobjectmodel/IXpsOMGlyphs::SetFontResource
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
 - IXpsOMGlyphs::SetFontResource
 - xpsobjectmodel/IXpsOMGlyphs::SetFontResource
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
 - IXpsOMGlyphs.SetFontResource
---

# IXpsOMGlyphs::SetFontResource


## -description

Sets the pointer to the  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a> interface of the font resource object that is required for this text.

## -parameters

### -param fontResource [in]

The pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a> interface to be used.

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
<i>fontResource</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>fontResource</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -remarks

<i>fontResource</i> must not be a <b>NULL</b> pointer; a glyph object must have a font resource.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresource">IXpsOMFontResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>