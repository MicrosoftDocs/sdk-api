---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetUnicodeString
title: IXpsOMGlyphs::GetUnicodeString (xpsobjectmodel.h)
description: Gets the text in unescaped UTF-16 scalar values. (IXpsOMGlyphs.GetUnicodeString)
helpviewer_keywords: ["GetUnicodeString","GetUnicodeString method [XPS Documents and Packaging]","GetUnicodeString method [XPS Documents and Packaging]","IXpsOMGlyphs interface","IXpsOMGlyphs interface [XPS Documents and Packaging]","GetUnicodeString method","IXpsOMGlyphs.GetUnicodeString","IXpsOMGlyphs::GetUnicodeString","xps.ixpsomglyphs_getunicodestring","xpsobjectmodel/IXpsOMGlyphs::GetUnicodeString"]
old-location: xps\ixpsomglyphs_getunicodestring.htm
tech.root: xps
ms.assetid: 0b1573b5-c9c7-4c7b-8511-c5c2fc42ed3e
ms.date: 12/05/2018
ms.keywords: GetUnicodeString, GetUnicodeString method [XPS Documents and Packaging], GetUnicodeString method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetUnicodeString method, IXpsOMGlyphs.GetUnicodeString, IXpsOMGlyphs::GetUnicodeString, xps.ixpsomglyphs_getunicodestring, xpsobjectmodel/IXpsOMGlyphs::GetUnicodeString
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
 - IXpsOMGlyphs::GetUnicodeString
 - xpsobjectmodel/IXpsOMGlyphs::GetUnicodeString
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
 - IXpsOMGlyphs.GetUnicodeString
---

# IXpsOMGlyphs::GetUnicodeString


## -description

Gets the text in unescaped UTF-16 scalar values.

## -parameters

### -param unicodeString [out, retval]

The UTF-16 Unicode string of the text to be displayed. If the string is empty, a <b>NULL</b> pointer is returned.

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
<i>unicodeString</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method allocates the memory that is used by the string returned in <i>unicodeString</i>.  If <i>unicodeString</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
