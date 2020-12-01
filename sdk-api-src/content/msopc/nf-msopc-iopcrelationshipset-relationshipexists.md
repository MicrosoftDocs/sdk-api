---
UID: NF:msopc.IOpcRelationshipSet.RelationshipExists
title: IOpcRelationshipSet::RelationshipExists (msopc.h)
description: Gets a value that indicates whether a specified relationship is represented as a relationship object in the set.
helpviewer_keywords: ["IOpcRelationshipSet interface [Open Packaging Conventions]","RelationshipExists method","IOpcRelationshipSet.RelationshipExists","IOpcRelationshipSet::RelationshipExists","RelationshipExists","RelationshipExists method [Open Packaging Conventions]","RelationshipExists method [Open Packaging Conventions]","IOpcRelationshipSet interface","msopc/IOpcRelationshipSet::RelationshipExists","opc.iopcrelationshipset_relationshipexists"]
old-location: opc\iopcrelationshipset_relationshipexists.htm
tech.root: OPC
ms.assetid: 18c989e2-8def-492d-ac57-014f9b6fcb22
ms.date: 12/05/2018
ms.keywords: IOpcRelationshipSet interface [Open Packaging Conventions],RelationshipExists method, IOpcRelationshipSet.RelationshipExists, IOpcRelationshipSet::RelationshipExists, RelationshipExists, RelationshipExists method [Open Packaging Conventions], RelationshipExists method [Open Packaging Conventions],IOpcRelationshipSet interface, msopc/IOpcRelationshipSet::RelationshipExists, opc.iopcrelationshipset_relationshipexists
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
 - IOpcRelationshipSet::RelationshipExists
 - msopc/IOpcRelationshipSet::RelationshipExists
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
 - IOpcRelationshipSet.RelationshipExists
---

# IOpcRelationshipSet::RelationshipExists


## -description

Gets a value that indicates whether a specified relationship  is represented as a relationship object in the set.

## -parameters

### -param relationshipIdentifier [in]

The unique identifier of a relationship.

### -param relationshipExists [out, retval]

One of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
A relationship that has the identifier specified in <i>relationshipIdentifier</i> is represented in the set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
A relationship that has the identifier specified in <i>relationshipIdentifier</i> is not represented in the set.

</td>
</tr>
</table>

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
At least one of the  <i>relationshipIdentifier</i> and <i>relationshipExists</i>  parameters is <b>NULL</b>.

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

If a relationship is represented in the set, the relationship is stored in the Relationships part represented by that set.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipset">IOpcRelationshipSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<b>Reference</b>