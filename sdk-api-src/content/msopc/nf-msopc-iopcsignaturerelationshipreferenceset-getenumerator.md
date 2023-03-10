---
UID: NF:msopc.IOpcSignatureRelationshipReferenceSet.GetEnumerator
title: IOpcSignatureRelationshipReferenceSet::GetEnumerator (msopc.h)
description: Gets an enumerator of IOpcSignatureRelationshipReference interface pointers in the set.
helpviewer_keywords: ["GetEnumerator","GetEnumerator method [Open Packaging Conventions]","GetEnumerator method [Open Packaging Conventions]","IOpcSignatureRelationshipReferenceSet interface","IOpcSignatureRelationshipReferenceSet interface [Open Packaging Conventions]","GetEnumerator method","IOpcSignatureRelationshipReferenceSet.GetEnumerator","IOpcSignatureRelationshipReferenceSet::GetEnumerator","msopc/IOpcSignatureRelationshipReferenceSet::GetEnumerator","opc.iopcsignaturerelationshipreferenceset_getenumerator"]
old-location: opc\iopcsignaturerelationshipreferenceset_getenumerator.htm
tech.root: OPC
ms.assetid: a574a935-f89a-445f-a793-d8dc2e116a48
ms.date: 12/05/2018
ms.keywords: GetEnumerator, GetEnumerator method [Open Packaging Conventions], GetEnumerator method [Open Packaging Conventions],IOpcSignatureRelationshipReferenceSet interface, IOpcSignatureRelationshipReferenceSet interface [Open Packaging Conventions],GetEnumerator method, IOpcSignatureRelationshipReferenceSet.GetEnumerator, IOpcSignatureRelationshipReferenceSet::GetEnumerator, msopc/IOpcSignatureRelationshipReferenceSet::GetEnumerator, opc.iopcsignaturerelationshipreferenceset_getenumerator
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
 - IOpcSignatureRelationshipReferenceSet::GetEnumerator
 - msopc/IOpcSignatureRelationshipReferenceSet::GetEnumerator
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
 - IOpcSignatureRelationshipReferenceSet.GetEnumerator
---

# IOpcSignatureRelationshipReferenceSet::GetEnumerator


## -description

Gets an enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointers in the set.

## -parameters

### -param relationshipReferenceEnumerator [out, retval]

A pointer to an enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointers in the set.

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
The <i>relationshipReferenceEnumerator</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreferenceenumerator">IOpcSignatureRelationshipReferenceEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreferenceset">IOpcSignatureRelationshipReferenceSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>