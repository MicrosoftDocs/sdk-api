---
UID: NN:msopc.IOpcSignatureRelationshipReference
title: IOpcSignatureRelationshipReference (msopc.h)
description: Represents a reference to a Relationships part that contains relationships that have been or will be signed.helpviewer_keywords: ["IOpcSignatureRelationshipReference","IOpcSignatureRelationshipReference interface [Open Packaging Conventions]","IOpcSignatureRelationshipReference interface [Open Packaging Conventions]","described","msopc/IOpcSignatureRelationshipReference","opc.iopcsignaturerelationshipreference"]
old-location: opc\iopcsignaturerelationshipreference.htm
tech.root: OPC
ms.assetid: 24aebfff-6b4f-49cb-988f-670ffed7d815
ms.date: 12/05/2018
ms.keywords: IOpcSignatureRelationshipReference, IOpcSignatureRelationshipReference interface [Open Packaging Conventions], IOpcSignatureRelationshipReference interface [Open Packaging Conventions],described, msopc/IOpcSignatureRelationshipReference, opc.iopcsignaturerelationshipreference
f1_keywords:
- msopc/IOpcSignatureRelationshipReference
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msopc.h
api_name:
- IOpcSignatureRelationshipReference
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOpcSignatureRelationshipReference interface


## -description


Represents a reference to a Relationships part that contains relationships that have been or will be signed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcSignatureRelationshipReference</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcSignatureRelationshipReference</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcSignatureRelationshipReference</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreference-getdigestmethod">GetDigestMethod</a>
</td>
<td align="left" width="63%">
Gets the digest method to use on relationship markup of the selected relationships.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreference-getdigestvalue">GetDigestValue</a>
</td>
<td align="left" width="63%">
Gets the digest value calculated for the selected relationships when they are signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreference-getrelationshipselectorenumerator">GetRelationshipSelectorEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselector">IOpcRelationshipSelector</a> interface pointers that represent the techniques used to select the subset of relationships in the referenced
               Relationships part.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreference-getrelationshipsigningoption">GetRelationshipSigningOption</a>
</td>
<td align="left" width="63%">
Gets a value that describes whether all or a subset of relationships that are stored in the referenced
               Relationships part are selected.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreference-getsourceuri">GetSourceUri</a>
</td>
<td align="left" width="63%">
Gets the  source URI of the relationships that are stored in the referenced  Relationships part.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreference-gettransformmethod">GetTransformMethod</a>
</td>
<td align="left" width="63%">
Gets the canonicalization method to use on the relationship markup of the selected relationships when they are signed.
            

</td>
</tr>
</table> 


## -remarks



 To create an  <b>IOpcSignatureRelationshipReference</b> interface pointer that represents a reference to a Relationships part, call the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceset-create">Create</a> method. This reference will indicate whether  all or a subset of the  relationships in the Relationships part will be signed when the signature is generated.

To access an <b>IOpcSignatureRelationshipReference</b> interface pointer, call the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceenumerator-getcurrent">IOpcSignatureRelationshipReferenceEnumerator::GetCurrent</a> method.

 Relationships that are not selected for signing can be removed, modified or added to  the package without invalidating the signature. If a subset of relationships has been selected for signing and the subset is altered, the signature will be invalidated.<div class="alert"><b>Important</b>  A selected subset could be altered if the relationship type of a relationship that is added to or modified in a referenced Relationships part matches a relationship type that was used to select one or more relationships in the subset.</div>
<div> </div>


The interface provides methods to access information about the referenced Relationships part, the selected relationships that have been or will be signed,  and the reference itself. When a signature is generated, this reference information is serialized in the XML markup of the signature (signature markup).  In signature markup, the information is represented by a  <b>Reference</b> element that has a <b>URI</b> attribute value that identifies a Relationships part.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreferenceenumerator">IOpcSignatureRelationshipReferenceEnumerator</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreferenceset">IOpcSignatureRelationshipReferenceSet</a>



<a href="https://docs.microsoft.com/windows/win32/api/msopc/ne-msopc-opc_canonicalization_method">OPC_CANONICALIZATION_METHOD</a>



<a href="https://docs.microsoft.com/windows/win32/api/msopc/ne-msopc-opc_relationships_signing_option">OPC_RELATIONSHIPS_SIGNING_OPTION</a>



<b>Overviews</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
 

 

