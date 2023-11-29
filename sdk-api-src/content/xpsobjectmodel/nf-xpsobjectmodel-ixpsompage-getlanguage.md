---
UID: NF:xpsobjectmodel.IXpsOMPage.GetLanguage
title: IXpsOMPage::GetLanguage (xpsobjectmodel.h)
description: Gets the Language property of the page.
helpviewer_keywords: ["GetLanguage","GetLanguage method [XPS Documents and Packaging]","GetLanguage method [XPS Documents and Packaging]","IXpsOMPage interface","IXpsOMPage interface [XPS Documents and Packaging]","GetLanguage method","IXpsOMPage.GetLanguage","IXpsOMPage::GetLanguage","xps.ixpsompage_getlanguage","xpsobjectmodel/IXpsOMPage::GetLanguage"]
old-location: xps\ixpsompage_getlanguage.htm
tech.root: xps
ms.assetid: d16378cc-dd1c-49f9-9c1b-1eb0d78067f7
ms.date: 12/05/2018
ms.keywords: GetLanguage, GetLanguage method [XPS Documents and Packaging], GetLanguage method [XPS Documents and Packaging],IXpsOMPage interface, IXpsOMPage interface [XPS Documents and Packaging],GetLanguage method, IXpsOMPage.GetLanguage, IXpsOMPage::GetLanguage, xps.ixpsompage_getlanguage, xpsobjectmodel/IXpsOMPage::GetLanguage
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
 - IXpsOMPage::GetLanguage
 - xpsobjectmodel/IXpsOMPage::GetLanguage
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
 - IXpsOMPage.GetLanguage
---

# IXpsOMPage::GetLanguage


## -description

Gets the <b>Language</b> property of the page.

## -parameters

### -param language [out, retval]

A language tag string that represents the language of the page contents. If the <b>Language</b> property has not been set, a <b>NULL</b> pointer is returned.

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

The default value is the language tag string that is passed to <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpage">IXpsOMObjectFactory::CreatePage</a>  in the <i>language</i>  parameter.

Internet Engineering Task Force (IETF) RFC 3066 describes the recommended encoding of the language tag string that is returned in <i>language</i>.

This method allocates the memory used by the string that is returned in <i>language</i>.  If <i>language</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="http://tools.ietf.org/html/rfc3066">The Internet Engineering Task Force (IETF) RFC 3066</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>