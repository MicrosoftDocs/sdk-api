---
UID: NF:msopc.IOpcRelationshipEnumerator.GetCurrent
title: IOpcRelationshipEnumerator::GetCurrent (msopc.h)
description: Gets the IOpcRelationship interface pointer at the current position of the enumerator.
helpviewer_keywords: ["GetCurrent","GetCurrent method [Open Packaging Conventions]","GetCurrent method [Open Packaging Conventions]","IOpcRelationshipEnumerator interface","IOpcRelationshipEnumerator interface [Open Packaging Conventions]","GetCurrent method","IOpcRelationshipEnumerator.GetCurrent","IOpcRelationshipEnumerator::GetCurrent","msopc/IOpcRelationshipEnumerator::GetCurrent","opc.iopcrelationshipenumerator_getcurrent"]
old-location: opc\iopcrelationshipenumerator_getcurrent.htm
tech.root: OPC
ms.assetid: 6ddd7a5f-659d-45e1-aff8-dee799efd8ac
ms.date: 12/05/2018
ms.keywords: GetCurrent, GetCurrent method [Open Packaging Conventions], GetCurrent method [Open Packaging Conventions],IOpcRelationshipEnumerator interface, IOpcRelationshipEnumerator interface [Open Packaging Conventions],GetCurrent method, IOpcRelationshipEnumerator.GetCurrent, IOpcRelationshipEnumerator::GetCurrent, msopc/IOpcRelationshipEnumerator::GetCurrent, opc.iopcrelationshipenumerator_getcurrent
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
 - IOpcRelationshipEnumerator::GetCurrent
 - msopc/IOpcRelationshipEnumerator::GetCurrent
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
 - IOpcRelationshipEnumerator.GetCurrent
---

# IOpcRelationshipEnumerator::GetCurrent


## -description

Gets the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointer at the current position of the enumerator.

## -parameters

### -param relationship [out, retval]

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship">IOpcRelationship</a> interface pointer.

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
The <i>partReference</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_ENUM_COLLECTION_CHANGED</b></dt>
<dt>0x80510050</dt>
</dl>
</td>
<td width="60%">
The enumerator is invalid because the underlying set has changed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_ENUM_INVALID_POSITION</b></dt>
<dt>0x80510053</dt>
</dl>
</td>
<td width="60%">
The enumerator cannot perform this operation from its current position.

</td>
</tr>
</table>

## -remarks

When an enumerator is created, the current position precedes the first pointer. To set the current position to the first pointer of the enumerator, call the  <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcrelationshipenumerator-movenext">MoveNext</a> method after creating the enumerator.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipenumerator">IOpcRelationshipEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipset">IOpcRelationshipSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-errors">Packaging Errors</a>



<b>Reference</b>