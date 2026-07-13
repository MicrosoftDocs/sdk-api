---
UID: NF:xpsobjectmodel.IXpsOMPage.SetLanguage
title: IXpsOMPage::SetLanguage (xpsobjectmodel.h)
description: Sets the Language property of the page.
helpviewer_keywords: ["IXpsOMPage interface [XPS Documents and Packaging]","SetLanguage method","IXpsOMPage.SetLanguage","IXpsOMPage::SetLanguage","SetLanguage","SetLanguage method [XPS Documents and Packaging]","SetLanguage method [XPS Documents and Packaging]","IXpsOMPage interface","xps.ixpsompage_setlanguage","xpsobjectmodel/IXpsOMPage::SetLanguage"]
old-location: xps\ixpsompage_setlanguage.htm
tech.root: xps
ms.assetid: 3bf0c7ed-84fc-45c0-8058-b833c3913f09
ms.date: 12/05/2018
ms.keywords: IXpsOMPage interface [XPS Documents and Packaging],SetLanguage method, IXpsOMPage.SetLanguage, IXpsOMPage::SetLanguage, SetLanguage, SetLanguage method [XPS Documents and Packaging], SetLanguage method [XPS Documents and Packaging],IXpsOMPage interface, xps.ixpsompage_setlanguage, xpsobjectmodel/IXpsOMPage::SetLanguage
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
 - IXpsOMPage::SetLanguage
 - xpsobjectmodel/IXpsOMPage::SetLanguage
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
 - IXpsOMPage.SetLanguage
---

# IXpsOMPage::SetLanguage


## -description

Sets the <b>Language</b> property of the page.

## -parameters

### -param language [in]

A language tag string that represents the language of the page content. A <b>NULL</b> pointer clears the previously assigned language.

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
<dt><b>XPS_E_INVALID_LANGUAGE</b></dt>
</dl>
</td>
<td width="60%">
The language string contains one or more language strings that are not valid. 

</td>
</tr>
</table>

## -remarks

The language tag string must conform to the language tag syntax that is described in the Internet Engineering Task Force (IETF) RFC 3066. For more information,  go to <a href="http://tools.ietf.org/html/rfc3066">http://tools.ietf.org/html/rfc3066</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="http://tools.ietf.org/html/rfc3066">The Internet Engineering Task Force (IETF) RFC 3066</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>