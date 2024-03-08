---
UID: NF:msopc.IOpcRelationshipSet.GetRelationshipsContentStream
title: IOpcRelationshipSet::GetRelationshipsContentStream (msopc.h)
description: Gets a read-only stream that contains the part content of the Relationships part represented by the set.
helpviewer_keywords: ["GetRelationshipsContentStream","GetRelationshipsContentStream method [Open Packaging Conventions]","GetRelationshipsContentStream method [Open Packaging Conventions]","IOpcRelationshipSet interface","IOpcRelationshipSet interface [Open Packaging Conventions]","GetRelationshipsContentStream method","IOpcRelationshipSet.GetRelationshipsContentStream","IOpcRelationshipSet::GetRelationshipsContentStream","msopc/IOpcRelationshipSet::GetRelationshipsContentStream","opc.iopcrelationshipset_getrelationshipscontentstream"]
old-location: opc\iopcrelationshipset_getrelationshipscontentstream.htm
tech.root: OPC
ms.assetid: 648e5bd1-25cc-48df-8120-ca1756eff8f7
ms.date: 12/05/2018
ms.keywords: GetRelationshipsContentStream, GetRelationshipsContentStream method [Open Packaging Conventions], GetRelationshipsContentStream method [Open Packaging Conventions],IOpcRelationshipSet interface, IOpcRelationshipSet interface [Open Packaging Conventions],GetRelationshipsContentStream method, IOpcRelationshipSet.GetRelationshipsContentStream, IOpcRelationshipSet::GetRelationshipsContentStream, msopc/IOpcRelationshipSet::GetRelationshipsContentStream, opc.iopcrelationshipset_getrelationshipscontentstream
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
 - IOpcRelationshipSet::GetRelationshipsContentStream
 - msopc/IOpcRelationshipSet::GetRelationshipsContentStream
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
 - IOpcRelationshipSet.GetRelationshipsContentStream
---

# IOpcRelationshipSet::GetRelationshipsContentStream


## -description

            Gets a read-only stream that contains the part content of the Relationships part represented by the set.

## -parameters

### -param contents [out, retval]

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface of the read-only  stream that contains the part content of the Relationships part represented by the set.

If  the relationships stored in the  Relationships part  have not been  modified, part content can include markup compatibility data that is not otherwise accessible through the relationship objects in the set.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>contents</i> parameter is <b>NULL</b>.

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

Calling this method will parse and validate all the relationships in the relationships markup. If the Relationships part contains invalid relationships markup, the markup cannot be retrieved by this method.

For more information about markup compatibility and packages, see Part 5: Markup Compatibility in <a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a> (https://www.ecma-international.org/publications-and-standards/standards/ecma-376/).


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipset">IOpcRelationshipSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a>