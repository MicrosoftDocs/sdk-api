---
UID: NN:msopc.IOpcSignatureRelationshipReferenceSet
title: IOpcSignatureRelationshipReferenceSet
author: windows-sdk-content
description: An unordered set of IOpcSignatureRelationshipReference interface pointers that represent references to Relationships parts that contain relationships to be signed.
old-location: opc\iopcsignaturerelationshipreferenceset.htm
tech.root: OPC
ms.assetid: 89ea7243-54ee-487b-a58a-0721af9db8c3
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IOpcSignatureRelationshipReferenceSet, IOpcSignatureRelationshipReferenceSet interface [Open Packaging Conventions], IOpcSignatureRelationshipReferenceSet interface [Open Packaging Conventions],described, msopc/IOpcSignatureRelationshipReferenceSet, opc.iopcsignaturerelationshipreferenceset
ms.prod: windows
ms.technology: windows-sdk
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
---

# IOpcSignatureRelationshipReferenceSet interface


## -description


An unordered set of <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointers that represent references to Relationships parts that contain relationships to be signed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcSignatureRelationshipReferenceSet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcSignatureRelationshipReferenceSet</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c348ac25-f2b3-491d-b378-f0daf282b1ca">Create</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointer that represents a reference to a Relationships part,  and adds the new interface pointer to the set.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b11f066-3e3a-4dd0-a938-853301bc6914">CreateRelationshipSelectorSet</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/cb23cbe2-764c-47e4-bd32-2791ddde9eee">IOpcRelationshipSelectorSet</a> interface pointer that is used as the <i>selectorSet</i> parameter value of the <a href="https://msdn.microsoft.com/c348ac25-f2b3-491d-b378-f0daf282b1ca">Create</a> method.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4f09a75-5c9d-4870-80e1-3c589435a6b7">Delete</a>
</td>
<td align="left" width="63%">
Deletes a specified  <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointer from the set.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a574a935-f89a-445f-a793-d8dc2e116a48">GetEnumerator</a>
</td>
<td align="left" width="63%">
Gets an enumerator of <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointers in the set.
            

</td>
</tr>
</table> 


## -remarks



 To create an  <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointer that represents a reference to a Relationships part, call the  <a href="https://msdn.microsoft.com/c348ac25-f2b3-491d-b378-f0daf282b1ca">Create</a> method. This reference will indicate whether  all or a subset of the  relationships in the Relationships part will be signed when the signature is generated.

To access an <b>IOpcSignatureRelationshipReferenceSet</b> interface pointer, call the <a href="https://msdn.microsoft.com/f89327d2-63ff-4b14-bde0-8fdf65f73e37">IOpcSigningOptions::GetSignatureRelationshipReferenceSet</a> method.

When an <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointer is created and added to the set, the reference it represents is saved when the package is saved.

When an <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointer is deleted from the set, the reference it represents is not saved when the package is saved.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



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
 

 

