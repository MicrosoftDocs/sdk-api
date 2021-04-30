---
UID: NF:msopc.IOpcRelationshipSelectorSet.Create
title: IOpcRelationshipSelectorSet::Create (msopc.h)
description: Creates an IOpcRelationshipSelector interface pointer to represent how a subset of relationships are selected to be signed, and adds the new pointer to the set.
helpviewer_keywords: ["Create","Create method [Open Packaging Conventions]","Create method [Open Packaging Conventions]","IOpcRelationshipSelectorSet interface","IOpcRelationshipSelectorSet interface [Open Packaging Conventions]","Create method","IOpcRelationshipSelectorSet.Create","IOpcRelationshipSelectorSet::Create","msopc/IOpcRelationshipSelectorSet::Create","opc.iopcrelationshipselectorset_create"]
old-location: opc\iopcrelationshipselectorset_create.htm
tech.root: OPC
ms.assetid: 801d1924-c75c-47b5-99fe-9d97ea8dfee1
ms.date: 12/05/2018
ms.keywords: Create, Create method [Open Packaging Conventions], Create method [Open Packaging Conventions],IOpcRelationshipSelectorSet interface, IOpcRelationshipSelectorSet interface [Open Packaging Conventions],Create method, IOpcRelationshipSelectorSet.Create, IOpcRelationshipSelectorSet::Create, msopc/IOpcRelationshipSelectorSet::Create, opc.iopcrelationshipselectorset_create
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
 - IOpcRelationshipSelectorSet::Create
 - msopc/IOpcRelationshipSelectorSet::Create
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
 - IOpcRelationshipSelectorSet.Create
---

# IOpcRelationshipSelectorSet::Create


## -description

Creates an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a> interface pointer to represent how a subset of relationships are selected to be signed, and adds the new pointer to the set.

## -parameters

### -param selector [in]

A value that describes how to interpret the  string that is passed in <i>selectionCriterion</i>.

### -param selectionCriterion [in]

A string that is interpreted to yield a criterion.

### -param relationshipSelector [out, retval]

A new <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a> interface pointer that represents how relationships are selected from a Relationships part.

This parameter can be <b>NULL</b> if a pointer to the  new interface is not needed.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value passed in the <i>selector</i> parameter is not a valid <a href="/windows/win32/api/msopc/ne-msopc-opc_relationship_selector">OPC_RELATIONSHIP_SELECTOR</a> enumeration value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>partUri</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Use the methods of the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a> interface pointers in the set to select relationships for signing.

When an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a> interface pointer is created and added to the set, the criterion it provides access to is saved when the package is saved.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselectorset">IOpcRelationshipSelectorSet</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_relationship_selector">OPC_RELATIONSHIP_SELECTOR</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>