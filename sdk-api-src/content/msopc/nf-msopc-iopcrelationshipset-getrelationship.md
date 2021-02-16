---
UID: NF:msopc.IOpcRelationshipSet.GetRelationship
title: IOpcRelationshipSet::GetRelationship (msopc.h)
description: Gets a relationship object from the set that represents a specified relationship.
helpviewer_keywords: ["GetRelationship","GetRelationship method [Open Packaging Conventions]","GetRelationship method [Open Packaging Conventions]","IOpcRelationshipSet interface","IOpcRelationshipSet interface [Open Packaging Conventions]","GetRelationship method","IOpcRelationshipSet.GetRelationship","IOpcRelationshipSet::GetRelationship","msopc/IOpcRelationshipSet::GetRelationship","opc.iopcrelationshipset_getrelationship"]
old-location: opc\iopcrelationshipset_getrelationship.htm
tech.root: OPC
ms.assetid: f44eeae6-592e-479e-98b7-f73075906a7a
ms.date: 12/05/2018
ms.keywords: GetRelationship, GetRelationship method [Open Packaging Conventions], GetRelationship method [Open Packaging Conventions],IOpcRelationshipSet interface, IOpcRelationshipSet interface [Open Packaging Conventions],GetRelationship method, IOpcRelationshipSet.GetRelationship, IOpcRelationshipSet::GetRelationship, msopc/IOpcRelationshipSet::GetRelationship, opc.iopcrelationshipset_getrelationship
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
 - IOpcRelationshipSet::GetRelationship
 - msopc/IOpcRelationshipSet::GetRelationship
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
 - IOpcRelationshipSet.GetRelationship
---

# IOpcRelationshipSet::GetRelationship


## -description

Gets a relationship object from the set that represents a specified relationship.

## -parameters

### -param relationshipIdentifier [in]

The unique identifier of a relationship.

### -param relationship [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface of the relationship object that represents the relationship that has the  specified identifier.

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
The <i>relationship</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_NO_SUCH_RELATIONSHIP</b></dt>
<dt>0x80510048</dt>
</dl>
</td>
<td width="60%">
The specified relationship does not exist.

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

The <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface provides access to relationship properties. For details about these properties, see the <a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a> and <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a>.


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



<a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a>