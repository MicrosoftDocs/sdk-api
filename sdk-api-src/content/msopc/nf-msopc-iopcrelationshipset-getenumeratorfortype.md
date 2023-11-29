---
UID: NF:msopc.IOpcRelationshipSet.GetEnumeratorForType
title: IOpcRelationshipSet::GetEnumeratorForType (msopc.h)
description: Gets an enumerator of the IOpcRelationship interface pointers in the set that point to representations of relationships that have a specified relationship type.
helpviewer_keywords: ["GetEnumeratorForType","GetEnumeratorForType method [Open Packaging Conventions]","GetEnumeratorForType method [Open Packaging Conventions]","IOpcRelationshipSet interface","IOpcRelationshipSet interface [Open Packaging Conventions]","GetEnumeratorForType method","IOpcRelationshipSet.GetEnumeratorForType","IOpcRelationshipSet::GetEnumeratorForType","msopc/IOpcRelationshipSet::GetEnumeratorForType","opc.iopcrelationshipset_getenumeratorfortype"]
old-location: opc\iopcrelationshipset_getenumeratorfortype.htm
tech.root: OPC
ms.assetid: 5b389660-f74d-48ae-a16b-5822661f0015
ms.date: 12/05/2018
ms.keywords: GetEnumeratorForType, GetEnumeratorForType method [Open Packaging Conventions], GetEnumeratorForType method [Open Packaging Conventions],IOpcRelationshipSet interface, IOpcRelationshipSet interface [Open Packaging Conventions],GetEnumeratorForType method, IOpcRelationshipSet.GetEnumeratorForType, IOpcRelationshipSet::GetEnumeratorForType, msopc/IOpcRelationshipSet::GetEnumeratorForType, opc.iopcrelationshipset_getenumeratorfortype
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
 - IOpcRelationshipSet::GetEnumeratorForType
 - msopc/IOpcRelationshipSet::GetEnumeratorForType
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
 - IOpcRelationshipSet.GetEnumeratorForType
---

# IOpcRelationshipSet::GetEnumeratorForType


## -description

            Gets an enumerator of the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointers in the set that point to representations of relationships  that have a specified relationship type.

## -parameters

### -param relationshipType [in]

The relationship type used to identify <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointers to be enumerated.

### -param relationshipEnumerator [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipenumerator">IOpcRelationshipEnumerator</a> interface of the  enumerator of the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointers in the set that point to representations of relationships  that have a specified relationship type.

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
At least one of the  <i>relationshipType</i> and <i>relationshipEnumerator</i>  parameters is <b>NULL</b>.

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

For information about forming the part name for the target of a relationship, see the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> topic.

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface provides access to relationship properties. For details about these properties, see the <a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a> and <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a>.

For more information about relationships, see <a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipset">IOpcRelationshipSet</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a>