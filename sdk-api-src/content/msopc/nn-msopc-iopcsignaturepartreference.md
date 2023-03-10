---
UID: NN:msopc.IOpcSignaturePartReference
title: IOpcSignaturePartReference (msopc.h)
description: Represents a reference to a part that has been or will be signed.
helpviewer_keywords: ["IOpcSignaturePartReference","IOpcSignaturePartReference interface [Open Packaging Conventions]","IOpcSignaturePartReference interface [Open Packaging Conventions]","described","msopc/IOpcSignaturePartReference","opc.iopcsignaturepartreference"]
old-location: opc\iopcsignaturepartreference.htm
tech.root: OPC
ms.assetid: b4bbf854-96b4-412b-a22d-c810423a3752
ms.date: 12/05/2018
ms.keywords: IOpcSignaturePartReference, IOpcSignaturePartReference interface [Open Packaging Conventions], IOpcSignaturePartReference interface [Open Packaging Conventions],described, msopc/IOpcSignaturePartReference, opc.iopcsignaturepartreference
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
 - IOpcSignaturePartReference
 - msopc/IOpcSignaturePartReference
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
 - IOpcSignaturePartReference
---

# IOpcSignaturePartReference interface


## -description

Represents a reference to a part that has been or will be signed.

## -inheritance

The <b>IOpcSignaturePartReference</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcSignaturePartReference</b> also has these types of members:

## -remarks

Only parts that can be represented by the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart">IOpcPart</a> interface can be referenced by an <b>IOpcSignaturePartReference</b> interface pointer. Relationships parts are referenced for signing  by a pointer to the <a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface. To create an <b>IOpcSignatureRelationshipReference</b> interface pointer, call the  <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceset-create">IOpcSignatureRelationshipReferenceSet::Create</a> method.

To create 
				an <b>IOpcSignaturePartReference</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturepartreferenceset-create">IOpcSignaturePartReferenceSet::Create</a> method.

To access an <b>IOpcSignaturePartReference</b> interface pointer, call the <a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturepartreferenceenumerator-getcurrent">IOpcSignaturePartReferenceEnumerator::GetCurrent</a> method.

The interface provides methods to access information about the referenced part and the reference itself. When a signature is generated, this reference information is serialized in the XML markup of the signature (signature markup).  In signature markup, the information is represented by a  <b>Reference</b> element that has its <b>URI</b> attribute value set to the part name of the referenced part.

The following markup shows that these <b>Reference</b> elements are children of the <b>Manifest</b> element in signature markup.


```xml
// Signature XML markup
<Signature>
	[...]
	// Package-specific <Object>
	<Object Id="idPackageObject">
		// This <Manifest> element contains only one signed part. 
		<Manifest>
			// A reference to a signed part.
			<Reference URI="aPartName">
				[...]
			</Reference>
		</Manifest>
		[...]
	</Object>
	[...]
</Signature>
```



#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.

## -see-also

<a href="/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreferenceenumerator">IOpcSignaturePartReferenceEnumerator</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturepartreferenceset">IOpcSignaturePartReferenceSet</a>



<a href="/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreferenceset">IOpcSignatureRelationshipReferenceSet</a>



<a href="/windows/win32/api/msopc/ne-msopc-opc_canonicalization_method">OPC_CANONICALIZATION_METHOD</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
