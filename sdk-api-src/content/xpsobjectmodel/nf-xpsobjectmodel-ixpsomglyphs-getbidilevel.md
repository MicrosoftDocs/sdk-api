---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetBidiLevel
title: IXpsOMGlyphs::GetBidiLevel (xpsobjectmodel.h)
description: Gets the level of bidirectional text.
helpviewer_keywords: ["GetBidiLevel","GetBidiLevel method [XPS Documents and Packaging]","GetBidiLevel method [XPS Documents and Packaging]","IXpsOMGlyphs interface","IXpsOMGlyphs interface [XPS Documents and Packaging]","GetBidiLevel method","IXpsOMGlyphs.GetBidiLevel","IXpsOMGlyphs::GetBidiLevel","xps.ixpsomglyphs_getbidilevel","xpsobjectmodel/IXpsOMGlyphs::GetBidiLevel"]
old-location: xps\ixpsomglyphs_getbidilevel.htm
tech.root: xps
ms.assetid: 17110bb7-1ae9-41ef-aed1-8f1c00569825
ms.date: 12/05/2018
ms.keywords: GetBidiLevel, GetBidiLevel method [XPS Documents and Packaging], GetBidiLevel method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetBidiLevel method, IXpsOMGlyphs.GetBidiLevel, IXpsOMGlyphs::GetBidiLevel, xps.ixpsomglyphs_getbidilevel, xpsobjectmodel/IXpsOMGlyphs::GetBidiLevel
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
 - IXpsOMGlyphs::GetBidiLevel
 - xpsobjectmodel/IXpsOMGlyphs::GetBidiLevel
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
 - IXpsOMGlyphs.GetBidiLevel
---

# IXpsOMGlyphs::GetBidiLevel


## -description

Gets the level of bidirectional text.

## -parameters

### -param bidiLevel [out, retval]

The level of bidirectional text.

Range: 0–61

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
<i>bidiLevel</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The bidirectional text level, or <b>BidiLevel</b>,  specifies the nesting level of the Unicode bidirectional algorithm. Even values imply the left-to-right layout and odd values the right-to-left layout, which places the run origin on the right side of the first glyph. Advance widths that are positive     will move to the left, allowing subsequent glyphs to be placed to the left of the previous glyph.

The range of allowed values for this property is between 0 and 61, inclusive, and the default value is 0.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>