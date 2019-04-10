---
UID: NF:msopc.IOpcSignatureRelationshipReferenceSet.Create
title: IOpcSignatureRelationshipReferenceSet::Create (msopc.h)
author: windows-sdk-content
description: Creates an IOpcSignatureRelationshipReference interface pointer that represents a reference to a Relationships part, and adds the new interface pointer to the set.
old-location: opc\iopcsignaturerelationshipreferenceset_create.htm
tech.root: OPC
ms.assetid: c348ac25-f2b3-491d-b378-f0daf282b1ca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Create, Create method [Open Packaging Conventions], Create method [Open Packaging Conventions],IOpcSignatureRelationshipReferenceSet interface, IOpcSignatureRelationshipReferenceSet interface [Open Packaging Conventions],Create method, IOpcSignatureRelationshipReferenceSet.Create, IOpcSignatureRelationshipReferenceSet::Create, msopc/IOpcSignatureRelationshipReferenceSet::Create, opc.iopcsignaturerelationshipreferenceset_create
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msopc.h
api_name:
 - IOpcSignatureRelationshipReferenceSet.Create
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcSignatureRelationshipReferenceSet::Create


## -description


Creates an <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointer that represents a reference to a Relationships part,  and adds the new interface pointer to the set. All or a subset of the relationships stored in the Relationships part to be referenced are selected for signing.


## -parameters




### -param sourceUri [in]

An <a href="https://msdn.microsoft.com/35ce7946-f7e7-4ac3-852f-e3fcca23d6d4">IOpcUri</a>  interface pointer that represents the source URI of the relationships to be selected for signing.


### -param digestMethod [in]

The digest method to be used for the relationships to be selected. To use the default digest method, pass <b>NULL</b> in this parameter.


<div class="alert"><b>Important</b>  The default digest method must be set by calling the <a href="https://msdn.microsoft.com/8de18a0e-cb3a-4232-90cb-718abdc9fb28">IOpcSigningOptions::SetDefaultDigestMethod</a> method before <a href="https://msdn.microsoft.com/5d40cae4-67d5-40a6-bd63-cf6243a703eb">IOpcDigitalSignatureManager::Sign</a> is called.</div>
<div> </div>



### -param relationshipSigningOption [in]

A value that indicates whether the relationships selected for signing include    all or a subset of the relationships in the Relationships part to be referenced.

For information about the effect of <i>relationshipSigningOption</i> values on other parameters, see Remarks.


### -param selectorSet [in]

An <a href="https://msdn.microsoft.com/cb23cbe2-764c-47e4-bd32-2791ddde9eee">IOpcRelationshipSelectorSet</a> interface pointer that can be used to identify a subset of relationships in the Relationships part to be selected for signing.

If <i>relationshipSigningOption</i> is  set to <b>OPC_RELATIONSHIP_SIGN_PART</b>, <i>selectorSet</i> is  <b>NULL</b>.

For information about <i>selectorSet</i> values, see Remarks.


### -param transformMethod [in]

A value that describes the canonicalization method to be applied to the relationship markup of the selected relationships.

If <i>relationshipSigningOption</i> is set <b>OPC_RELATIONSHIP_SIGN_USING_SELECTORS</b>, the value of <i>transformMethod</i> is ignored.

For more information about the transform methods to be applied when  <i>relationshipSigningOption</i>  is set to <b>OPC_RELATIONSHIP_SIGN_USING_SELECTORS</b>, see Remarks.


### -param relationshipReference [out, retval]

A new <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointer that represents the referenced Relationships part.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value passed in the <i>relationshipSigningOption</i> parameter is not a valid <a href="https://msdn.microsoft.com/b6a83730-459a-4119-a013-7d670e659c32">OPC_RELATIONSHIPS_SIGNING_OPTION</a> enumeration value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The value passed in the <i>transformMethod</i> parameter is not a valid <a href="https://msdn.microsoft.com/f8401d12-da2e-4b35-b473-ebe3d1f91abd">OPC_CANONICALIZATION_METHOD</a> enumeration value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>sourceUri</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>selectorSet</i> parameter is not being passed <b>NULL</b> while the <i>relationshipSigningOption</i> parameter is passed a value of <b>OPC_RELATIONSHIP_SIGN_PART</b>.

</td>
</tr>
</table>
 




## -remarks



This method creates a reference to a Relationships part. All or a subset of the  relationships that are stored in a referenced Relationships part can be signed when the signature is generated.

To sign all of the relationships in a Relationships part, call this method with the <i>relationshipSigningOption</i> parameter value set to <b>OPC_RELATIONSHIP_SIGN_PART</b> and the <i>selectorSet</i> parameter value set to <b>NULL</b>.

To sign a subset of the relationships in a Relationships part, call this method with the <i>relationshipSigningOption</i> parameter value set to <b>OPC_RELATIONSHIP_SIGN_USING_SELECTORS</b> and the <i>selectorSet</i> parameter value set to an <a href="https://msdn.microsoft.com/cb23cbe2-764c-47e4-bd32-2791ddde9eee">IOpcRelationshipSelectorSet</a> interface pointer. To create an <b>IOpcRelationshipSelectorSet</b> interface pointer, call the <a href="https://msdn.microsoft.com/7b11f066-3e3a-4dd0-a938-853301bc6914">CreateRelationshipSelectorSet</a> method.

The following table summarizes the parameter values required by this method to create a reference that indicates whether all of the relationships or a subset of the relationships (which are stored in the Relationships part to be referenced) are to be signed.<table>
<tr>
<th>Description</th>
<th><i>relationshipSigningOption</i> Value</th>
<th><i>selectorSet</i> Value</th>
</tr>
<tr>
<td>Sign all of the relationships in the Relationships part</td>
<td><b>OPC_RELATIONSHIP_SIGN_PART</b></td>
<td><b>NULL</b></td>
</tr>
<tr>
<td>Sign a subset of the relationships in the Relationships part</td>
<td><b>OPC_RELATIONSHIP_SIGN_USING_SELECTORS</b></td>
<td>An <a href="https://msdn.microsoft.com/cb23cbe2-764c-47e4-bd32-2791ddde9eee">IOpcRelationshipSelectorSet</a> interface pointer</td>
</tr>
</table>
 



If a subset of relationships are to be signed, the specified transform method is ignored.  Instead, when the signature is generated, the first transform applied is the Relationships Transform, and the second is the  <b>OPC_CANONICALIZATION_C14N</b> canonicalization method.

When an <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointer is created and added to the set, the reference it represents is saved when the package is saved.

 Relationships that will not be signed can be removed, modified or added to  the package without invalidating the signature. If a subset of relationships has been selected for signing and the subset is altered, the signature will be invalidated.

<div class="alert"><b>Important</b>  A selected subset could be altered if the relationship type of a relationship that is added to or modified in a referenced Relationships part matches a relationship type that was used to select one or more relationships in the subset.</div>
<div> </div>

#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/13e8a7b9-1d25-421b-bc81-adc495e6d9c7">IOpcDigitalSignatureManager</a>



<a href="https://msdn.microsoft.com/89ea7243-54ee-487b-a58a-0721af9db8c3">IOpcSignatureRelationshipReferenceSet</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<a href="https://msdn.microsoft.com/f8401d12-da2e-4b35-b473-ebe3d1f91abd">OPC_CANONICALIZATION_METHOD</a>



<a href="https://msdn.microsoft.com/b6a83730-459a-4119-a013-7d670e659c32">OPC_RELATIONSHIPS_SIGNING_OPTION</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

