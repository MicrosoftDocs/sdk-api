---
UID: NF:msopc.IOpcPart.GetRelationshipSet
title: IOpcPart::GetRelationshipSet (msopc.h)
description: Gets a relationship set object that represents the Relationships part that stores relationships that have the part as their source.
helpviewer_keywords: ["GetRelationshipSet","GetRelationshipSet method [Open Packaging Conventions]","GetRelationshipSet method [Open Packaging Conventions]","IOpcPart interface","IOpcPart interface [Open Packaging Conventions]","GetRelationshipSet method","IOpcPart.GetRelationshipSet","IOpcPart::GetRelationshipSet","msopc/IOpcPart::GetRelationshipSet","opc.iopcpart_getrelationshipset"]
old-location: opc\iopcpart_getrelationshipset.htm
tech.root: OPC
ms.assetid: a8a8ce1f-3420-457f-b02a-5dc3e9725a02
ms.date: 12/05/2018
ms.keywords: GetRelationshipSet, GetRelationshipSet method [Open Packaging Conventions], GetRelationshipSet method [Open Packaging Conventions],IOpcPart interface, IOpcPart interface [Open Packaging Conventions],GetRelationshipSet method, IOpcPart.GetRelationshipSet, IOpcPart::GetRelationshipSet, msopc/IOpcPart::GetRelationshipSet, opc.iopcpart_getrelationshipset
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
 - IOpcPart::GetRelationshipSet
 - msopc/IOpcPart::GetRelationshipSet
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
 - IOpcPart.GetRelationshipSet
---

# IOpcPart::GetRelationshipSet


## -description

Gets a relationship set object that represents the Relationships part that stores relationships that have the part as their source.

## -parameters

### -param relationshipSet [out, retval]

A pointer to a relationship set object that represents the Relationships part  that stores all relationships that have the part as their source.

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
The <i>relationshipSet</i> parameter is <b>NULL</b>.

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

The definitive way to find a part of interest is by using a relationship type to find the relationship that has the part of interest as its target. The target's URI can then be resolved to a part name which is used to access the part.

For more information about using the relationship type to find a relationship and then a part of interest, see <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipset">IOpcRelationshipSet</a> and <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a>.

For more information about parts and relationships, see the <a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a> and the <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i>.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="https://www.ecma-international.org/publications-and-standards/standards/ecma-376/">ECMA-376 OpenXML</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<a href="/previous-versions/windows/desktop/opc/parts-overview">Parts Overview</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a>