---
UID: NF:msopc.IOpcSignatureCustomObjectSet.Create
title: IOpcSignatureCustomObjectSet::Create (msopc.h)
description: Creates an IOpcSignatureCustomObject interface pointer to represent an application-specific Object element in the signature, and adds the new interface to the set.
helpviewer_keywords: ["Create","Create method [Open Packaging Conventions]","Create method [Open Packaging Conventions]","IOpcSignatureCustomObjectSet interface","IOpcSignatureCustomObjectSet interface [Open Packaging Conventions]","Create method","IOpcSignatureCustomObjectSet.Create","IOpcSignatureCustomObjectSet::Create","msopc/IOpcSignatureCustomObjectSet::Create","opc.iopcsignaturecustomobjectset_create"]
old-location: opc\iopcsignaturecustomobjectset_create.htm
tech.root: OPC
ms.assetid: 93bf4509-900c-42bc-9834-c8a33cfe7e65
ms.date: 12/05/2018
ms.keywords: Create, Create method [Open Packaging Conventions], Create method [Open Packaging Conventions],IOpcSignatureCustomObjectSet interface, IOpcSignatureCustomObjectSet interface [Open Packaging Conventions],Create method, IOpcSignatureCustomObjectSet.Create, IOpcSignatureCustomObjectSet::Create, msopc/IOpcSignatureCustomObjectSet::Create, opc.iopcsignaturecustomobjectset_create
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OpcDigitalSignature.idl
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
 - IOpcSignatureCustomObjectSet::Create
 - msopc/IOpcSignatureCustomObjectSet::Create
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcSignatureCustomObjectSet.Create
---

# IOpcSignatureCustomObjectSet::Create


## -description

Creates an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointer to represent an application-specific <b>Object</b> element in the signature, and adds the new interface to the set.

## -parameters

### -param xmlMarkup [in]

A buffer that contains the XML markup for the <b>Object</b> element to be represented.

This XML markup must include the opening <b>Object</b> and closing <b>/Object</b> tags.

The encoding of the markup contained in <i>xmlMarkup</i> will be inferred. Inclusion of a <a href="/previous-versions/ms776429(v=vs.85)">byte order mark</a> at the beginning of the buffer passed in <i>xmlMarkup</i> is optional.

The following encodings and <a href="/previous-versions/ms776429(v=vs.85)">byte order mark</a> values are supported:<table>
<tr>
<th>Encoding</th>
<th>Description</th>
<th>Byte order mark</th>
</tr>
<tr>
<td>UTF8</td>
<td>UTF-8</td>
<td>EF BB BF</td>
</tr>
<tr>
<td>UTF16LE</td>
<td>UTF-16, little endian</td>
<td>FF FE</td>
</tr>
<tr>
<td>UTF16BE</td>
<td>UTF-16, big endian</td>
<td>FE FF</td>
</tr>
</table>

### -param count [in]

The size of the <i>xmlMarkup</i> buffer.

### -param customObject [out, retval]

A new <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointer that represents the application-specific <b>Object</b> element.

This parameter can be <b>NULL</b> if a pointer to the  new interface is not needed.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>count</i> parameter is 0. The <i>xmlMarkup</i> parameter must be passed valid XML markup.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>xmlMarkup</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointer provides access to the XML markup of the <b>Object</b> element it represents. To access the XML markup of the  <b>Object</b> element, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturecustomobject-getxml">IOpcSignatureCustomObject::GetXml</a> method.

When an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobject">IOpcSignatureCustomObject</a> interface pointer is created and added to the set, the <b>Object</b>  it represents is saved when the package is saved.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturecustomobjectset">IOpcSignatureCustomObjectSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>