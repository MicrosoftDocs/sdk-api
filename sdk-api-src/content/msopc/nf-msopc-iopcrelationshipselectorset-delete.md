---
UID: NF:msopc.IOpcRelationshipSelectorSet.Delete
title: IOpcRelationshipSelectorSet::Delete (msopc.h)
description: Deletes a specified IOpcRelationshipSelector interface pointer from the set.
helpviewer_keywords: ["Delete","Delete method [Open Packaging Conventions]","Delete method [Open Packaging Conventions]","IOpcRelationshipSelectorSet interface","IOpcRelationshipSelectorSet interface [Open Packaging Conventions]","Delete method","IOpcRelationshipSelectorSet.Delete","IOpcRelationshipSelectorSet::Delete","msopc/IOpcRelationshipSelectorSet::Delete","opc.iopcrelationshipselectorset_delete"]
old-location: opc\iopcrelationshipselectorset_delete.htm
tech.root: OPC
ms.assetid: a90757f7-bdb1-4cff-9a46-64ec953f2172
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Open Packaging Conventions], Delete method [Open Packaging Conventions],IOpcRelationshipSelectorSet interface, IOpcRelationshipSelectorSet interface [Open Packaging Conventions],Delete method, IOpcRelationshipSelectorSet.Delete, IOpcRelationshipSelectorSet::Delete, msopc/IOpcRelationshipSelectorSet::Delete, opc.iopcrelationshipselectorset_delete
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
 - IOpcRelationshipSelectorSet::Delete
 - msopc/IOpcRelationshipSelectorSet::Delete
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
 - IOpcRelationshipSelectorSet.Delete
---

# IOpcRelationshipSelectorSet::Delete


## -description

Deletes a specified <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a> interface pointer from the set.

## -parameters

### -param relationshipSelector [in]

An <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a> interface pointer to be deleted.

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
The <i>relationshipSelector</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

When an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a> interface pointer is deleted from the set, the criterion it provides access to is not saved when the package is saved.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselectorset">IOpcRelationshipSelectorSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>