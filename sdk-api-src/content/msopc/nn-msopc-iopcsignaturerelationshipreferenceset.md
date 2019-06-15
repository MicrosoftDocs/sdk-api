---
UID: NN:msopc.IOpcSignatureRelationshipReferenceSet
title: IOpcSignatureRelationshipReferenceSet (msopc.h)
author: windows-sdk-content
description: An unordered set of IOpcSignatureRelationshipReference interface pointers that represent references to Relationships parts that contain relationships to be signed.
old-location: opc\iopcsignaturerelationshipreferenceset.htm
tech.root: OPC
ms.assetid: 89ea7243-54ee-487b-a58a-0721af9db8c3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOpcSignatureRelationshipReferenceSet, IOpcSignatureRelationshipReferenceSet interface [Open Packaging Conventions], IOpcSignatureRelationshipReferenceSet interface [Open Packaging Conventions],described, msopc/IOpcSignatureRelationshipReferenceSet, opc.iopcsignaturerelationshipreferenceset
ms.topic: interface
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
 - IOpcSignatureRelationshipReferenceSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOpcSignatureRelationshipReferenceSet interface


## -description


An unordered set of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointers that represent references to Relationships parts that contain relationships to be signed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcSignatureRelationshipReferenceSet</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOpcSignatureRelationshipReferenceSet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcSignatureRelationshipReferenceSet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceset-create">Create</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointer that represents a reference to a Relationships part,  and adds the new interface pointer to the set.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceset-createrelationshipselectorset">CreateRelationshipSelectorSet</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipselectorset">IOpcRelationshipSelectorSet</a> interface pointer that is used as the <i>selectorSet</i> parameter value of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceset-create">Create</a> method.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceset-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes a specified  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointer from the set.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceset-getenumerator">GetEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointers in the set.
            

</td>
</tr>
</table> 


## -remarks



 To create an  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointer that represents a reference to a Relationships part, call the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsignaturerelationshipreferenceset-create">Create</a> method. This reference will indicate whether  all or a subset of the  relationships in the Relationships part will be signed when the signature is generated.

To access an <b>IOpcSignatureRelationshipReferenceSet</b> interface pointer, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcsigningoptions-getsignaturerelationshipreferenceset">IOpcSigningOptions::GetSignatureRelationshipReferenceSet</a> method.

When an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointer is created and added to the set, the reference it represents is saved when the package is saved.

When an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsignaturerelationshipreference">IOpcSignatureRelationshipReference</a> interface pointer is deleted from the set, the reference it represents is not saved when the package is saved.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/core-packaging-interfaces">Core Packaging Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/digital-signatures-overview">Digital Signatures Overview</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcsigningoptions">IOpcSigningOptions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/ne-msopc-__midl___midl_itf_msopc_0001_0076_0001">OPC_CANONICALIZATION_METHOD</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/ne-msopc-__midl___midl_itf_msopc_0001_0076_0003">OPC_RELATIONSHIPS_SIGNING_OPTION</a>



<b>Overviews</b>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-reference">Packaging API Reference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/opc/packaging-digital-signature-interfaces">Packaging Digital Signature Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
 

 

