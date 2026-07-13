---
UID: NN:msopc.IOpcPart
title: IOpcPart (msopc.h)
description: Represents a part that contains data and is not a Relationships part.
helpviewer_keywords: ["IOpcPart","IOpcPart interface [Open Packaging Conventions]","IOpcPart interface [Open Packaging Conventions]","described","msopc/IOpcPart","opc.iopcpart"]
old-location: opc\iopcpart.htm
tech.root: OPC
ms.assetid: e6a40f30-03d1-4c93-a5e0-563b4c6588b4
ms.date: 12/05/2018
ms.keywords: IOpcPart, IOpcPart interface [Open Packaging Conventions], IOpcPart interface [Open Packaging Conventions],described, msopc/IOpcPart, opc.iopcpart
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
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
 - IOpcPart
 - msopc/IOpcPart
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
 - IOpcPart
---

# IOpcPart interface


## -description

Represents a part that contains data and is not a Relationships part.

## -inheritance

The <b>IOpcPart</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcPart</b> also has these types of members:

## -remarks

To create a part object to represent a part, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcpartset-createpart">IOpcPartSet::CreatePart</a> method. To get a pointer to the interface of a part object that represents an existing part, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcpartset-getpart">IOpcPartSet::GetPart</a> or  <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcpartenumerator-getcurrent">IOpcPartEnumerator::GetCurrent</a> method.

A Relationships part cannot be represented by an implementation of the <b>IOpcPart</b> interface.

Methods of an <b>IOpcPart</b> interface provide access to part information through the properties listed in the following table:

<table>
<tr>
<th>Method</th>
<th>Property</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcpart-getcompressionoptions">GetCompressionOptions</a>
</td>
<td>Compression </td>
<td>
The compression option to be used on part content.

</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcpart-getcontentstream">GetContentStream</a>
</td>
<td>Content</td>
<td>
The stream of bytes that makes up the part as described in the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.

</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcpart-getcontenttype">GetContentType</a>
</td>
<td>Content type</td>
<td>
The media type of the part content, as specified by the package designer in compliance with the rules in the <i>OPC</i>.

</td>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcpart-getname">GetName</a>
</td>
<td>Name</td>
<td>
The URI of the part in the package. 

</td>
</tr>
</table>
 

For more information about parts, see the <a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>OPC</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpartset">IOpcPartSet</a>



<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_compression_options">OPC_COMPRESSION_OPTIONS</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a>



<b>Reference</b>
