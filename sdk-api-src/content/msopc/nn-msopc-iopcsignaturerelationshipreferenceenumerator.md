---
UID: NN:msopc.IOpcSignatureRelationshipReferenceEnumerator
title: IOpcSignatureRelationshipReferenceEnumerator (msopc.h)
description: A read-only enumerator of IOpcSignatureRelationshipReference interface pointers.
helpviewer_keywords: ["IOpcSignatureRelationshipReferenceEnumerator","IOpcSignatureRelationshipReferenceEnumerator interface [Open Packaging Conventions]","IOpcSignatureRelationshipReferenceEnumerator interface [Open Packaging Conventions]","described","msopc/IOpcSignatureRelationshipReferenceEnumerator","opc.iopcsignaturerelationshipreferenceenumerator"]
old-location: opc\iopcsignaturerelationshipreferenceenumerator.htm
tech.root: OPC
ms.assetid: aa4c6e8b-1a1f-464b-885e-bee0976afafc
ms.date: 12/05/2018
ms.keywords: IOpcSignatureRelationshipReferenceEnumerator, IOpcSignatureRelationshipReferenceEnumerator interface [Open Packaging Conventions], IOpcSignatureRelationshipReferenceEnumerator interface [Open Packaging Conventions],described, msopc/IOpcSignatureRelationshipReferenceEnumerator, opc.iopcsignaturerelationshipreferenceenumerator
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IOpcSignatureRelationshipReferenceEnumerator
 - msopc/IOpcSignatureRelationshipReferenceEnumerator
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
 - IOpcSignatureRelationshipReferenceEnumerator
---

# IOpcSignatureRelationshipReferenceEnumerator interface


## -description

A read-only enumerator of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointers.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcSignatureRelationshipReferenceEnumerator</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcSignatureRelationshipReferenceEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcSignatureRelationshipReferenceEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceenumerator-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the current <b>IOpcSignatureRelationshipReferenceEnumerator</b> interface pointer and all its descendants.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceenumerator-getcurrent">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointer at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceenumerator-movenext">MoveNext</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the next <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceenumerator-moveprevious">MovePrevious</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the previous <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointer.

</td>
</tr>
</table>

## -remarks

When an enumerator is created, the current position precedes the first pointer. To set the current position to the first pointer of the enumerator, call the  <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceenumerator-movenext">MoveNext</a>method after creating the enumerator.

Changes to the set will invalidate the enumerator and all subsequent calls to it will fail.

To get an <b>IOpcSignatureRelationshipReferenceEnumerator</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceset-getenumerator">IOpcSignatureRelationshipReferenceSet::GetEnumerator</a> or <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcdigitalsignature-getsignaturerelationshipreferenceenumerator">IOpcDigitalSignature::GetSignatureRelationshipReferenceEnumerator</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcdigitalsignature">IOpcDigitalSignature</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreferenceset">IOpcSignatureRelationshipReferenceSet</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>