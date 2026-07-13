---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.GetKeywords
title: IXpsOMCoreProperties::GetKeywords (xpsobjectmodel.h)
description: Gets the keywords property.
helpviewer_keywords: ["GetKeywords","GetKeywords method [XPS Documents and Packaging]","GetKeywords method [XPS Documents and Packaging]","IXpsOMCoreProperties interface","IXpsOMCoreProperties interface [XPS Documents and Packaging]","GetKeywords method","IXpsOMCoreProperties.GetKeywords","IXpsOMCoreProperties::GetKeywords","xps.ixpsomcoreproperties_getkeywords","xpsobjectmodel/IXpsOMCoreProperties::GetKeywords"]
old-location: xps\ixpsomcoreproperties_getkeywords.htm
tech.root: xps
ms.assetid: f0bac4c7-5bb6-4a9d-8f16-db97e7efee5a
ms.date: 12/05/2018
ms.keywords: GetKeywords, GetKeywords method [XPS Documents and Packaging], GetKeywords method [XPS Documents and Packaging],IXpsOMCoreProperties interface, IXpsOMCoreProperties interface [XPS Documents and Packaging],GetKeywords method, IXpsOMCoreProperties.GetKeywords, IXpsOMCoreProperties::GetKeywords, xps.ixpsomcoreproperties_getkeywords, xpsobjectmodel/IXpsOMCoreProperties::GetKeywords
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
 - IXpsOMCoreProperties::GetKeywords
 - xpsobjectmodel/IXpsOMCoreProperties::GetKeywords
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
 - IXpsOMCoreProperties.GetKeywords
---

# IXpsOMCoreProperties::GetKeywords


## -description

Gets the <b>keywords</b> property.

## -parameters

### -param keywords [out, retval]

The string that is read from the <b>keywords</b> property.

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
<i>keywords</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The <b>keywords</b> property is a delimited set of keywords that are used to support searching and
indexing. This is typically a list of terms that are not
available in other properties.

This method allocates the memory used by the string that is returned in <i>keywords</i>.  If <i>keywords</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>