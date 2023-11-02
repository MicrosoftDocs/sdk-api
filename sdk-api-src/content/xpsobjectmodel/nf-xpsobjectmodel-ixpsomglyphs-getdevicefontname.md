---
UID: NF:xpsobjectmodel.IXpsOMGlyphs.GetDeviceFontName
title: IXpsOMGlyphs::GetDeviceFontName (xpsobjectmodel.h)
description: Gets the name of the device font. (IXpsOMGlyphs.GetDeviceFontName)
helpviewer_keywords: ["GetDeviceFontName","GetDeviceFontName method [XPS Documents and Packaging]","GetDeviceFontName method [XPS Documents and Packaging]","IXpsOMGlyphs interface","IXpsOMGlyphs interface [XPS Documents and Packaging]","GetDeviceFontName method","IXpsOMGlyphs.GetDeviceFontName","IXpsOMGlyphs::GetDeviceFontName","xps.ixpsomglyphs_getdevicefontname","xpsobjectmodel/IXpsOMGlyphs::GetDeviceFontName"]
old-location: xps\ixpsomglyphs_getdevicefontname.htm
tech.root: xps
ms.assetid: cb288d73-da4d-4b46-95e5-c451c9ee2dc7
ms.date: 12/05/2018
ms.keywords: GetDeviceFontName, GetDeviceFontName method [XPS Documents and Packaging], GetDeviceFontName method [XPS Documents and Packaging],IXpsOMGlyphs interface, IXpsOMGlyphs interface [XPS Documents and Packaging],GetDeviceFontName method, IXpsOMGlyphs.GetDeviceFontName, IXpsOMGlyphs::GetDeviceFontName, xps.ixpsomglyphs_getdevicefontname, xpsobjectmodel/IXpsOMGlyphs::GetDeviceFontName
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
 - IXpsOMGlyphs::GetDeviceFontName
 - xpsobjectmodel/IXpsOMGlyphs::GetDeviceFontName
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
 - IXpsOMGlyphs.GetDeviceFontName
---

# IXpsOMGlyphs::GetDeviceFontName


## -description

Gets the name of the  device font.

## -parameters

### -param deviceFontName [out, retval]

The string that contains the unescaped name of the  device font. If the name has not been set, a <b>NULL</b> pointer will be returned.

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
<i>deviceFontName</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The device font name uniquely identifies a specific device font and is typically defined by a hardware vendor or font vendor.

The escaped version of the device font name is created when the object is serialized.

This method allocates the memory used by the string that is returned in <i>deviceFontName</i>.  If <i>deviceFontName</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs">IXpsOMGlyphs</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
