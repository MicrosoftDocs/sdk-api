---
UID: NF:msopc.IOpcSignatureRelationshipReferenceSet.CreateRelationshipSelectorSet
title: IOpcSignatureRelationshipReferenceSet::CreateRelationshipSelectorSet (msopc.h)
description: Creates an IOpcRelationshipSelectorSet interface pointer that is used as the selectorSet parameter value of the Create method.
helpviewer_keywords: ["CreateRelationshipSelectorSet","CreateRelationshipSelectorSet method [Open Packaging Conventions]","CreateRelationshipSelectorSet method [Open Packaging Conventions]","IOpcSignatureRelationshipReferenceSet interface","IOpcSignatureRelationshipReferenceSet interface [Open Packaging Conventions]","CreateRelationshipSelectorSet method","IOpcSignatureRelationshipReferenceSet.CreateRelationshipSelectorSet","IOpcSignatureRelationshipReferenceSet::CreateRelationshipSelectorSet","msopc/IOpcSignatureRelationshipReferenceSet::CreateRelationshipSelectorSet","opc.iopcsignaturerelationshipreferenceset_createrelationshipselectorset"]
old-location: opc\iopcsignaturerelationshipreferenceset_createrelationshipselectorset.htm
tech.root: OPC
ms.assetid: 7b11f066-3e3a-4dd0-a938-853301bc6914
ms.date: 12/05/2018
ms.keywords: CreateRelationshipSelectorSet, CreateRelationshipSelectorSet method [Open Packaging Conventions], CreateRelationshipSelectorSet method [Open Packaging Conventions],IOpcSignatureRelationshipReferenceSet interface, IOpcSignatureRelationshipReferenceSet interface [Open Packaging Conventions],CreateRelationshipSelectorSet method, IOpcSignatureRelationshipReferenceSet.CreateRelationshipSelectorSet, IOpcSignatureRelationshipReferenceSet::CreateRelationshipSelectorSet, msopc/IOpcSignatureRelationshipReferenceSet::CreateRelationshipSelectorSet, opc.iopcsignaturerelationshipreferenceset_createrelationshipselectorset
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
 - IOpcSignatureRelationshipReferenceSet::CreateRelationshipSelectorSet
 - msopc/IOpcSignatureRelationshipReferenceSet::CreateRelationshipSelectorSet
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
 - IOpcSignatureRelationshipReferenceSet.CreateRelationshipSelectorSet
---

# IOpcSignatureRelationshipReferenceSet::CreateRelationshipSelectorSet


## -description

Creates an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselectorset">IOpcRelationshipSelectorSet</a> interface pointer that is used as the <i>selectorSet</i> parameter value of the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceset-create">Create</a> method.

## -parameters

### -param selectorSet [out]

A new <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselectorset">IOpcRelationshipSelectorSet</a> interface pointer.

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
The <i>selectorSet</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

To select a subset of the relationships (which are stored in the Relationships part to be referenced) to be signed when the signature is generated, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceset-create">Create</a> method with the <i>relationshipSigningOption</i> parameter value set to <b>OPC_RELATIONSHIP_SIGN_USING_SELECTORS</b> and the <i>selectorSet</i> parameter value set to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselectorset">IOpcRelationshipSelectorSet</a> interface pointer created by this method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreferenceset">IOpcSignatureRelationshipReferenceSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>