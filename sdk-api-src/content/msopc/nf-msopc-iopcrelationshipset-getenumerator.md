---
UID: NF:msopc.IOpcRelationshipSet.GetEnumerator
title: IOpcRelationshipSet::GetEnumerator (msopc.h)
description: Gets an enumerator of IOpcRelationship interface pointers in the set.
helpviewer_keywords: ["GetEnumerator","GetEnumerator method [Open Packaging Conventions]","GetEnumerator method [Open Packaging Conventions]","IOpcRelationshipSet interface","IOpcRelationshipSet interface [Open Packaging Conventions]","GetEnumerator method","IOpcRelationshipSet.GetEnumerator","IOpcRelationshipSet::GetEnumerator","msopc/IOpcRelationshipSet::GetEnumerator","opc.iopcrelationshipset_getenumerator"]
old-location: opc\iopcrelationshipset_getenumerator.htm
tech.root: OPC
ms.assetid: bcffa20d-b86e-4bfe-9f67-7404d44acb03
ms.date: 12/05/2018
ms.keywords: GetEnumerator, GetEnumerator method [Open Packaging Conventions], GetEnumerator method [Open Packaging Conventions],IOpcRelationshipSet interface, IOpcRelationshipSet interface [Open Packaging Conventions],GetEnumerator method, IOpcRelationshipSet.GetEnumerator, IOpcRelationshipSet::GetEnumerator, msopc/IOpcRelationshipSet::GetEnumerator, opc.iopcrelationshipset_getenumerator
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
 - IOpcRelationshipSet::GetEnumerator
 - msopc/IOpcRelationshipSet::GetEnumerator
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
 - IOpcRelationshipSet.GetEnumerator
---

# IOpcRelationshipSet::GetEnumerator


## -description

Gets an enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointers in the set.

## -parameters

### -param relationshipEnumerator [out, retval]

A pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipenumerator">IOpcRelationshipEnumerator</a> interface of the enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointers in the set.

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
The <i>relationshipEnumerator</i> parameter is <b>NULL</b>.

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

## -see-also

<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipset">IOpcRelationshipSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a>