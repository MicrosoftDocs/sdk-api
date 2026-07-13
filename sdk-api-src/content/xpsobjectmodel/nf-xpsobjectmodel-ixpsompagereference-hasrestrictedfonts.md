---
UID: NF:xpsobjectmodel.IXpsOMPageReference.HasRestrictedFonts
title: IXpsOMPageReference::HasRestrictedFonts (xpsobjectmodel.h)
description: Gets a Boolean value that indicates whether the document sub-tree of the referenced page includes any Glyphs that have a font resource whose EmbeddingOption property is set to XPS_FONT_EMBEDDING_RESTRICTED.
helpviewer_keywords: ["FALSE","HasRestrictedFonts","HasRestrictedFonts method [XPS Documents and Packaging]","HasRestrictedFonts method [XPS Documents and Packaging]","IXpsOMPageReference interface","IXpsOMPageReference interface [XPS Documents and Packaging]","HasRestrictedFonts method","IXpsOMPageReference.HasRestrictedFonts","IXpsOMPageReference::HasRestrictedFonts","TRUE","xps.ixpsompagereference_hasrestrictedfonts","xpsobjectmodel/IXpsOMPageReference::HasRestrictedFonts"]
old-location: xps\ixpsompagereference_hasrestrictedfonts.htm
tech.root: xps
ms.assetid: 721dffd7-a15f-4028-be9e-854a4445d76d
ms.date: 12/05/2018
ms.keywords: FALSE, HasRestrictedFonts, HasRestrictedFonts method [XPS Documents and Packaging], HasRestrictedFonts method [XPS Documents and Packaging],IXpsOMPageReference interface, IXpsOMPageReference interface [XPS Documents and Packaging],HasRestrictedFonts method, IXpsOMPageReference.HasRestrictedFonts, IXpsOMPageReference::HasRestrictedFonts, TRUE, xps.ixpsompagereference_hasrestrictedfonts, xpsobjectmodel/IXpsOMPageReference::HasRestrictedFonts
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
 - IXpsOMPageReference::HasRestrictedFonts
 - xpsobjectmodel/IXpsOMPageReference::HasRestrictedFonts
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
 - IXpsOMPageReference.HasRestrictedFonts
---

# IXpsOMPageReference::HasRestrictedFonts


## -description

Gets a Boolean value that indicates whether the document sub-tree of the referenced page includes any Glyphs that have a font resource whose  <b>EmbeddingOption</b> property is set to <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_font_embedding">XPS_FONT_EMBEDDING_RESTRICTED</a>.

## -parameters

### -param restrictedFonts [out, retval]

A Boolean value that indicates whether the document sub-tree of the referenced page includes any <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a> interfaces that have a font resource whose  <b>EmbeddingOption</b> property is set to <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_font_embedding">XPS_FONT_EMBEDDING_RESTRICTED</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
If the referenced page is loaded,  the page references at least one font resource whose <b>EmbeddingOption</b> property is set to <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_font_embedding">XPS_FONT_EMBEDDING_RESTRICTED</a>.

If the referenced page is not loaded, it has a relationship with at least one font resource whose <b>EmbeddingOption</b> property is set to   <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_font_embedding">XPS_FONT_EMBEDDING_RESTRICTED</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
If the referenced page is loaded,  the page does not reference any font resources whose <b>EmbeddingOption</b> property is set to <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_font_embedding">XPS_FONT_EMBEDDING_RESTRICTED</a>.

If the referenced page is not loaded, it does not have a relationship with a font resource whose <b>EmbeddingOption</b> property is set to   <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_font_embedding">XPS_FONT_EMBEDDING_RESTRICTED</a>.

</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

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
<i>restrictedFonts</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This value is not updated automatically. If fonts or glyphs are added or removed such that the value changes, <b>HasRestrictedFonts</b> must be called again to get the current value.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_font_embedding">XPS_FONT_EMBEDDING_RESTRICTED</a>