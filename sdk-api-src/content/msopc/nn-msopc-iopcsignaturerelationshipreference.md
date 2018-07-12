---
UID: NN:msopc.IOpcSignatureRelationshipReference
title: IOpcSignatureRelationshipReference
author: windows-sdk-content
description: Represents a reference to a Relationships part that contains relationships that have been or will be signed.
old-location: opc\iopcsignaturerelationshipreference.htm
old-project: OPC
ms.assetid: 24aebfff-6b4f-49cb-988f-670ffed7d815
ms.author: windowssdkdev
ms.date: 03/15/2018
ms.keywords: IOpcSignatureRelationshipReference, IOpcSignatureRelationshipReference interface [Open Packaging Conventions], IOpcSignatureRelationshipReference interface [Open Packaging Conventions],described, msopc/IOpcSignatureRelationshipReference, opc.iopcsignaturerelationshipreference
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcSignatureRelationshipReference
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcSignatureRelationshipReference interface


## -description


Represents a reference to a Relationships part that contains relationships that have been or will be signed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcSignatureRelationshipReference</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcSignatureRelationshipReference</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/126e0b2c-8b58-4b42-b2b5-99f6fab40f27">GetDigestMethod</a>
</td>
<td align="left" width="63%">

              Gets the digest method to use on relationship markup of the selected relationships.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c1f3e73-45fc-4325-bc7a-db9241385c4e">GetDigestValue</a>
</td>
<td align="left" width="63%">

              Gets the digest value calculated for the selected relationships when they are signed.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9e1e9e8-d318-4e72-ba52-d020e58f85ff">GetRelationshipSelectorEnumerator</a>
</td>
<td align="left" width="63%">

              Gets an enumerator of <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a> interface pointers that represent the techniques used to select the subset of relationships in the referenced
               
              Relationships part.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9960c67c-4f09-435e-b82c-ca449645f6e5">GetRelationshipSigningOption</a>
</td>
<td align="left" width="63%">

              Gets a value that describes whether all or a subset of relationships that are stored in the referenced
               
              Relationships part are selected.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d08cfbf0-0917-4ca4-85be-5ca62d7029d0">GetSourceUri</a>
</td>
<td align="left" width="63%">

              Gets the  source URI of the relationships that are stored in the referenced  
              Relationships part.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87d85f7e-abf2-4f6f-91b6-36a014cc0f33">GetTransformMethod</a>
</td>
<td align="left" width="63%">

              Gets the canonicalization method to use on the relationship markup of the selected relationships when they are signed.
            

</td>
</tr>
</table> 


## -remarks



 To create an  <b>IOpcSignatureRelationshipReference</b> interface pointer that represents a reference to a Relationships part, call the  <a href="https://msdn.microsoft.com/c348ac25-f2b3-491d-b378-f0daf282b1ca">Create</a> method. This reference will indicate whether  all or a subset of the  relationships in the Relationships part will be signed when the signature is generated.

To access an <b>IOpcSignatureRelationshipReference</b> interface pointer, call the  <a href="https://msdn.microsoft.com/18aac7c9-db1a-4fc5-896e-7a02c12788f2">IOpcSignatureRelationshipReferenceEnumerator::GetCurrent</a> method.

 Relationships that are not selected for signing can be removed, modified or added to  the package without invalidating the signature. If a subset of relationships has been selected for signing and the subset is altered, the signature will be invalidated.<div class="alert"><b>Important</b>  A selected subset could be altered if the relationship type of a relationship that is added to or modified in a referenced Relationships part matches a relationship type that was used to select one or more relationships in the subset.</div>
<div> </div>


The interface provides methods to access information about the referenced Relationships part, the selected relationships that have been or will be signed,  and the reference itself. When a signature is generated, this reference information is serialized in the XML markup of the signature (signature markup).  In signature markup, the information is represented by a  <b>Reference</b> element that has a <b>URI</b> attribute value that identifies a Relationships part.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/aa4c6e8b-1a1f-464b-885e-bee0976afafc">IOpcSignatureRelationshipReferenceEnumerator</a>



<a href="https://msdn.microsoft.com/89ea7243-54ee-487b-a58a-0721af9db8c3">IOpcSignatureRelationshipReferenceSet</a>



<a href="https://msdn.microsoft.com/f8401d12-da2e-4b35-b473-ebe3d1f91abd">OPC_CANONICALIZATION_METHOD</a>



<a href="https://msdn.microsoft.com/b6a83730-459a-4119-a013-7d670e659c32">OPC_RELATIONSHIPS_SIGNING_OPTION</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

