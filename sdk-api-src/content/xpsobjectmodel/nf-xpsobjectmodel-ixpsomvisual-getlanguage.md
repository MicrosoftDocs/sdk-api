---
UID: NF:xpsobjectmodel.IXpsOMVisual.GetLanguage
title: IXpsOMVisual::GetLanguage (xpsobjectmodel.h)
description: Gets the Language property of the visual and of its contents.
helpviewer_keywords: ["GetLanguage","GetLanguage method [XPS Documents and Packaging]","GetLanguage method [XPS Documents and Packaging]","IXpsOMVisual interface","IXpsOMVisual interface [XPS Documents and Packaging]","GetLanguage method","IXpsOMVisual.GetLanguage","IXpsOMVisual::GetLanguage","xps.ixpsomvisual_getlanguage","xpsobjectmodel/IXpsOMVisual::GetLanguage"]
old-location: xps\ixpsomvisual_getlanguage.htm
tech.root: xps
ms.assetid: 22cddce5-f881-4585-9ab8-d8cdce06511f
ms.date: 12/05/2018
ms.keywords: GetLanguage, GetLanguage method [XPS Documents and Packaging], GetLanguage method [XPS Documents and Packaging],IXpsOMVisual interface, IXpsOMVisual interface [XPS Documents and Packaging],GetLanguage method, IXpsOMVisual.GetLanguage, IXpsOMVisual::GetLanguage, xps.ixpsomvisual_getlanguage, xpsobjectmodel/IXpsOMVisual::GetLanguage
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
 - IXpsOMVisual::GetLanguage
 - xpsobjectmodel/IXpsOMVisual::GetLanguage
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
 - IXpsOMVisual.GetLanguage
---

# IXpsOMVisual::GetLanguage


## -description

Gets the <b>Language</b> property of the visual and of its contents.

## -parameters

### -param language [out, retval]

The language string that specifies the language of the page. If a language has not been set, a <b>NULL</b> pointer is returned.

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
<i>language</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The <b>Language</b> property that is set by this method specifies the language of the resource content.

This method allocates the memory that is used by the string returned in <i>language</i>.  If <i>language</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

Internet Engineering Task Force (IETF) RFC 3066 specifies the recommended encoding for the <b>Language</b> property.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>