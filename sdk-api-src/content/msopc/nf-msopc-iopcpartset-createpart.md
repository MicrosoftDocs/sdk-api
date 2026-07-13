---
UID: NF:msopc.IOpcPartSet.CreatePart
title: IOpcPartSet::CreatePart (msopc.h)
description: Creates a part object that represents a part and adds a pointer to the object's IOpcPart interface to the set.
helpviewer_keywords: ["CreatePart","CreatePart method [Open Packaging Conventions]","CreatePart method [Open Packaging Conventions]","IOpcPartSet interface","IOpcPartSet interface [Open Packaging Conventions]","CreatePart method","IOpcPartSet.CreatePart","IOpcPartSet::CreatePart","msopc/IOpcPartSet::CreatePart","opc.iopcpartset_createpart"]
old-location: opc\iopcpartset_createpart.htm
tech.root: OPC
ms.assetid: 8c5de7ac-f51c-42f2-9068-8e9ede86ad97
ms.date: 12/05/2018
ms.keywords: CreatePart, CreatePart method [Open Packaging Conventions], CreatePart method [Open Packaging Conventions],IOpcPartSet interface, IOpcPartSet interface [Open Packaging Conventions],CreatePart method, IOpcPartSet.CreatePart, IOpcPartSet::CreatePart, msopc/IOpcPartSet::CreatePart, opc.iopcpartset_createpart
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Opcobjectmodel.idl
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
 - IOpcPartSet::CreatePart
 - msopc/IOpcPartSet::CreatePart
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
 - IOpcPartSet.CreatePart
---

# IOpcPartSet::CreatePart


## -description

Creates a part object that represents a part and adds a pointer to the object's <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> interface to the set.

## -parameters

### -param name [in]

A pointer to the  <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface of a part URI object that represents the part name of the part.

To create  a part URI object (which implements the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a> interface) to represent the part name of the part, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcfactory-createparturi">IOpcFactory::CreatePartUri</a> method.

### -param contentType [in]

The media type of part content.

### -param compressionOptions [in]

A value that describes the way to compress the part content of the part.

### -param part [out, retval]

A pointer to the new <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> that represents the part.

This parameter cannot be <b>NULL</b>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code/value</th>
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
The <i>name</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value passed in the <i>compressionOptions</i> parameter is not a valid <a href="/windows/win32/api/msopc/ne-msopc-opc_compression_options">OPC_COMPRESSION_OPTIONS</a> enumeration value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_DUPLICATE_PART</b></dt>
<dt>0x8051000B</dt>
</dl>
</td>
<td width="60%">
A part with the specified part name already exists in the current package.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_INVALID_CONTENT_TYPE</b></dt>
<dt>0x80510044</dt>
</dl>
</td>
<td width="60%">
A content type does not conform to the rules for a valid media type, specified in <a href="https://www.w3.org/Protocols/rfc2616/rfc2616.html">RFC 2616: HTTP/1.1</a> (http://www.w3.org/Protocols/rfc2616/rfc2616.html) and the <i>OPC</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_UNEXPECTED_CONTENT_TYPE</b></dt>
<dt>0x80510005</dt>
</dl>
</td>
<td width="60%">
Either the content type of a part differed from the expected content type (specified in the OPC, <a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 Part 2</a>), or the part content did not match the part's  content type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Package Consumption error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="/previous-versions/windows/desktop/opc/package-consumption-error-group">Package Consumption Error Group</a>.
        

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Part URI error</b></dt>
</dl>
</td>
<td width="60%">
An <b>HRESULT</b> error code from the <a href="/previous-versions/windows/desktop/opc/part-uri-error-group">Part URI Error Group</a>.
        

</td>
</tr>
</table>

## -remarks

When a part object is created and a pointer to it is added to the set, the part it represents is serialized when the package is serialized.

This method cannot create a part object that represents a Relationships part.

If part content is compressed prior to the creation of the part object, pass the <b>OPC_COMPRESSION_NONE</b> value in the <i>compressionOptions</i> parameter.

Part content that is already compressed will not compress significantly more.

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> provides access to the properties of a part. For details about these properties, see the <a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a> and the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> topic.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcfactory-createparturi">IOpcFactory::CreatePartUri</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpartset">IOpcPartSet</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_compression_options">OPC_COMPRESSION_OPTIONS</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a>



<a href="https://www.w3.org/Protocols/rfc2616/rfc2616.html">RFC 2616: HTTP/1.1</a>



<b>Reference</b>