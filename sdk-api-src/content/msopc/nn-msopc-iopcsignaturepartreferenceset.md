---
UID: NN:msopc.IOpcSignaturePartReferenceSet
title: IOpcSignaturePartReferenceSet (msopc.h)
description: An unordered set of IOpcSignaturePartReference interface pointers that represent references to parts to be signed.
helpviewer_keywords: ["IOpcSignaturePartReferenceSet","IOpcSignaturePartReferenceSet interface [Open Packaging Conventions]","IOpcSignaturePartReferenceSet interface [Open Packaging Conventions]","described","msopc/IOpcSignaturePartReferenceSet","opc.iopcsignaturepartreferenceset"]
old-location: opc\iopcsignaturepartreferenceset.htm
tech.root: OPC
ms.assetid: c6f453e4-e0f5-4ecc-b622-6b30778ff719
ms.date: 12/05/2018
ms.keywords: IOpcSignaturePartReferenceSet, IOpcSignaturePartReferenceSet interface [Open Packaging Conventions], IOpcSignaturePartReferenceSet interface [Open Packaging Conventions],described, msopc/IOpcSignaturePartReferenceSet, opc.iopcsignaturepartreferenceset
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
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
 - IOpcSignaturePartReferenceSet
 - msopc/IOpcSignaturePartReferenceSet
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
 - IOpcSignaturePartReferenceSet
---

# IOpcSignaturePartReferenceSet interface


## -description

An unordered set of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreference">IOpcSignaturePartReference</a> interface pointers that represent references to parts to be signed.

## -inheritance

The <b>IOpcSignaturePartReferenceSet</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcSignaturePartReferenceSet</b> also has these types of members:

## -remarks

Only parts that can be represented by the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> interface can be referenced by an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreference">IOpcSignaturePartReference</a> interface pointer. Relationships parts are referenced for signing  by a pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface. To create an <b>IOpcSignatureRelationshipReference</b> interface pointer, call the  <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceset-create">IOpcSignatureRelationshipReferenceSet::Create</a> method.

When an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreference">IOpcSignaturePartReference</a> interface pointer is created and added to the set, the reference it represents is saved when the package is saved.

When an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreference">IOpcSignaturePartReference</a> interface pointer is deleted from the set, the reference it represents is not saved when the package is saved.

To create an <b>IOpcSignaturePartReferenceSet</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getsignaturepartreferenceset">IOpcSigningOptions::GetSignaturePartReferenceSet</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreferenceset">IOpcSignatureRelationshipReferenceSet</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_canonicalization_method">OPC_CANONICALIZATION_METHOD</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
