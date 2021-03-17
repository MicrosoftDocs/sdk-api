---
UID: NF:msopc.IOpcDigitalSignature.GetSignatureRelationshipReferenceEnumerator
title: IOpcDigitalSignature::GetSignatureRelationshipReferenceEnumerator (msopc.h)
description: Gets an enumerator of IOpcSignatureRelationshipReference interface pointers, which represent references to relationships that have been signed.
helpviewer_keywords: ["GetSignatureRelationshipReferenceEnumerator","GetSignatureRelationshipReferenceEnumerator method [Open Packaging Conventions]","GetSignatureRelationshipReferenceEnumerator method [Open Packaging Conventions]","IOpcDigitalSignature interface","IOpcDigitalSignature interface [Open Packaging Conventions]","GetSignatureRelationshipReferenceEnumerator method","IOpcDigitalSignature.GetSignatureRelationshipReferenceEnumerator","IOpcDigitalSignature::GetSignatureRelationshipReferenceEnumerator","msopc/IOpcDigitalSignature::GetSignatureRelationshipReferenceEnumerator","opc.iopcdigitalsignature_getsignaturerelationshipreferenceenumerator"]
old-location: opc\iopcdigitalsignature_getsignaturerelationshipreferenceenumerator.htm
tech.root: OPC
ms.assetid: ffb74828-1177-4c3d-8a8c-e40bb0c4cbf0
ms.date: 12/05/2018
ms.keywords: GetSignatureRelationshipReferenceEnumerator, GetSignatureRelationshipReferenceEnumerator method [Open Packaging Conventions], GetSignatureRelationshipReferenceEnumerator method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetSignatureRelationshipReferenceEnumerator method, IOpcDigitalSignature.GetSignatureRelationshipReferenceEnumerator, IOpcDigitalSignature::GetSignatureRelationshipReferenceEnumerator, msopc/IOpcDigitalSignature::GetSignatureRelationshipReferenceEnumerator, opc.iopcdigitalsignature_getsignaturerelationshipreferenceenumerator
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
 - IOpcDigitalSignature::GetSignatureRelationshipReferenceEnumerator
 - msopc/IOpcDigitalSignature::GetSignatureRelationshipReferenceEnumerator
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
 - IOpcDigitalSignature.GetSignatureRelationshipReferenceEnumerator
---

# IOpcDigitalSignature::GetSignatureRelationshipReferenceEnumerator


## -description

Gets an enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointers, which represent references to relationships that have been signed.

## -parameters

### -param relationshipReferenceEnumerator [out, retval]

A pointer to an enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointers, which represent references to relationships that have been signed.

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



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreferenceenumerator">IOpcSignatureRelationshipReferenceEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreferenceset">IOpcSignatureRelationshipReferenceSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>