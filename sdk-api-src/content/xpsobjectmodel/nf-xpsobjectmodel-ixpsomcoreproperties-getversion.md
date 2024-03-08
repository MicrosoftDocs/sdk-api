---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.GetVersion
title: IXpsOMCoreProperties::GetVersion (xpsobjectmodel.h)
description: Gets the version property.
helpviewer_keywords: ["GetVersion","GetVersion method [XPS Documents and Packaging]","GetVersion method [XPS Documents and Packaging]","IXpsOMCoreProperties interface","IXpsOMCoreProperties interface [XPS Documents and Packaging]","GetVersion method","IXpsOMCoreProperties.GetVersion","IXpsOMCoreProperties::GetVersion","xps.ixpsomcoreproperties_getversion","xpsobjectmodel/IXpsOMCoreProperties::GetVersion"]
old-location: xps\ixpsomcoreproperties_getversion.htm
tech.root: xps
ms.assetid: d0a693e5-fd98-47c0-aaf7-f8461169a01c
ms.date: 12/05/2018
ms.keywords: GetVersion, GetVersion method [XPS Documents and Packaging], GetVersion method [XPS Documents and Packaging],IXpsOMCoreProperties interface, IXpsOMCoreProperties interface [XPS Documents and Packaging],GetVersion method, IXpsOMCoreProperties.GetVersion, IXpsOMCoreProperties::GetVersion, xps.ixpsomcoreproperties_getversion, xpsobjectmodel/IXpsOMCoreProperties::GetVersion
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
 - IXpsOMCoreProperties::GetVersion
 - xpsobjectmodel/IXpsOMCoreProperties::GetVersion
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
 - IXpsOMCoreProperties.GetVersion
---

# IXpsOMCoreProperties::GetVersion


## -description

Gets the <b>version</b> property.

## -parameters

### -param version [out, retval]

The string that is read from the <b>version</b> property.

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
<i>version</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The <b>version</b> property contains the resource's version number.

This method allocates the memory used by the string that is returned in <i>version</i>.  If <i>version</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>