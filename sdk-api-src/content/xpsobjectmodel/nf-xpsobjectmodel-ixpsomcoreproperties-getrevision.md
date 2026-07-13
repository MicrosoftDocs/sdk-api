---
UID: NF:xpsobjectmodel.IXpsOMCoreProperties.GetRevision
title: IXpsOMCoreProperties::GetRevision (xpsobjectmodel.h)
description: Gets the revision property.
helpviewer_keywords: ["GetRevision","GetRevision method [XPS Documents and Packaging]","GetRevision method [XPS Documents and Packaging]","IXpsOMCoreProperties interface","IXpsOMCoreProperties interface [XPS Documents and Packaging]","GetRevision method","IXpsOMCoreProperties.GetRevision","IXpsOMCoreProperties::GetRevision","xps.ixpsomcoreproperties_getrevision","xpsobjectmodel/IXpsOMCoreProperties::GetRevision"]
old-location: xps\ixpsomcoreproperties_getrevision.htm
tech.root: xps
ms.assetid: 7143e4e7-c5e3-41f8-84d8-64fa3008ccc8
ms.date: 12/05/2018
ms.keywords: GetRevision, GetRevision method [XPS Documents and Packaging], GetRevision method [XPS Documents and Packaging],IXpsOMCoreProperties interface, IXpsOMCoreProperties interface [XPS Documents and Packaging],GetRevision method, IXpsOMCoreProperties.GetRevision, IXpsOMCoreProperties::GetRevision, xps.ixpsomcoreproperties_getrevision, xpsobjectmodel/IXpsOMCoreProperties::GetRevision
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
 - IXpsOMCoreProperties::GetRevision
 - xpsobjectmodel/IXpsOMCoreProperties::GetRevision
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
 - IXpsOMCoreProperties.GetRevision
---

# IXpsOMCoreProperties::GetRevision


## -description

Gets the <b>revision</b> property.

## -parameters

### -param revision [out, retval]

The string that is read from the <b>revision</b> property.

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
<i>revision</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The <b>revision</b> property contains the resource's revision number.

This method allocates the memory used by the string that is returned in <i>revision</i>.  If <i>revision</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcoreproperties">IXpsOMCoreProperties</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">Standard ECMA-376, Office Open XML File Formats</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>