---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.SetOrigin
title: IXpsOMGlyphs::SetOrigin (xpsobjectmodel.h)
description: Sets the starting position of the text.
helpviewer_keywords: ["IXpsOMGlyphs interface [XPS Documents and Packaging]","SetOrigin method","IXpsOMGlyphs.SetOrigin","IXpsOMGlyphs::SetOrigin","SetOrigin","SetOrigin method [XPS Documents and Packaging]","SetOrigin method [XPS Documents and Packaging]","IXpsOMGlyphs interface","xps.ixpsomglyphs_setorigin","xpsobjectmodel/IXpsOMGlyphs::SetOrigin"]
old-location: xps\ixpsomglyphs_setorigin.htm
tech.root: xps
ms.assetid: f5491bf0-bc40-491e-bf5e-f3fb580e10b4
ms.date: 12/05/2018
ms.keywords: IXpsOMGlyphs interface [XPS Documents and Packaging],SetOrigin method, IXpsOMGlyphs.SetOrigin, IXpsOMGlyphs::SetOrigin, SetOrigin, SetOrigin method [XPS Documents and Packaging], SetOrigin method [XPS Documents and Packaging],IXpsOMGlyphs interface, xps.ixpsomglyphs_setorigin, xpsobjectmodel/IXpsOMGlyphs::SetOrigin
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
 - IXpsOMGlyphs::SetOrigin
 - xpsobjectmodel/IXpsOMGlyphs::SetOrigin
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
 - IXpsOMGlyphs.SetOrigin
---

# IXpsOMGlyphs::SetOrigin


## -description

Sets the starting position of the text.

## -parameters

### -param origin [in]

The <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_point">XPS_POINT</a> structure that contains the coordinates to be set as the text's starting position.

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
<i>origin</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>origin.x</i> or <i>origin.y</i> refers to a floating-point value that is not valid.

</td>
</tr>
</table>

## -remarks

In the units of the effective coordinate space, the origin specifies the x and y coordinates of the first glyph in the run. The glyph is placed such that its baseline and the leading edge of its advance vector intersect with the point defined by <i>origin.x</i> and <i>origin.y</i>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_point">XPS_POINT</a>