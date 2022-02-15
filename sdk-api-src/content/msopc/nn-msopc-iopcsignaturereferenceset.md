---
UID: NN:msopc.IOpcSignatureReferenceSet
title: IOpcSignatureReferenceSet (msopc.h)
description: An unordered set of IOpcSignatureReference interface pointers that represent references to XML elements to be signed.
helpviewer_keywords: ["IOpcSignatureReferenceSet","IOpcSignatureReferenceSet interface [Open Packaging Conventions]","IOpcSignatureReferenceSet interface [Open Packaging Conventions]","described","msopc/IOpcSignatureReferenceSet","opc.iopcsignaturereferenceset"]
old-location: opc\iopcsignaturereferenceset.htm
tech.root: OPC
ms.assetid: 7955ac86-de6e-4911-a107-a1617c14e685
ms.date: 12/05/2018
ms.keywords: IOpcSignatureReferenceSet, IOpcSignatureReferenceSet interface [Open Packaging Conventions], IOpcSignatureReferenceSet interface [Open Packaging Conventions],described, msopc/IOpcSignatureReferenceSet, opc.iopcsignaturereferenceset
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
 - IOpcSignatureReferenceSet
 - msopc/IOpcSignatureReferenceSet
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
 - IOpcSignatureReferenceSet
---

# IOpcSignatureReferenceSet interface


## -description

An unordered set of <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a> interface pointers that represent references to XML elements  to be signed.  An XML element to be signed can be either an application-specific <b>Object</b> element or a child element.

## -inheritance

The <b>IOpcSignatureReferenceSet</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcSignatureReferenceSet</b> also has these types of members:

## -remarks

The <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturereferenceset-create">Create</a> method creates a reference to an application-specific <b>Object</b> element or a child of an application-specific <b>Object</b> that is signed when the signature is generated. <b>Create</b> does not create the reference to the package-specific <b>Object</b> element to be signed; that reference is created automatically when the signature is generated.

When an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a> interface pointer is created and added to the set, the reference it represents is saved when the package is saved.

When an <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturereference">IOpcSignatureReference</a> interface pointer is deleted from the set, the reference it represents is not saved when the package is saved.

To access an <b>IOpcSignatureReferenceSet</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getcustomreferenceset">IOpcSigningOptions::GetCustomReferenceSet</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_canonicalization_method">OPC_CANONICALIZATION_METHOD</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
