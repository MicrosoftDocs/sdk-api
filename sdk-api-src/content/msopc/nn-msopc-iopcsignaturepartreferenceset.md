---
UID: NN:msopc.IOpcSignaturePartReferenceSet
title: IOpcSignaturePartReferenceSet
author: windows-driver-content
description: An unordered set of IOpcSignaturePartReference interface pointers that represent references to parts to be signed.
old-location: opc\iopcsignaturepartreferenceset.htm
old-project: OPC
ms.assetid: c6f453e4-e0f5-4ecc-b622-6b30778ff719
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IOpcSignaturePartReferenceSet, IOpcSignaturePartReferenceSet interface [Open Packaging Conventions], IOpcSignaturePartReferenceSet interface [Open Packaging Conventions],described, msopc/IOpcSignaturePartReferenceSet, opc.iopcsignaturepartreferenceset
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msopc.h
api_name:
-	IOpcSignaturePartReferenceSet
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOpcSignaturePartReferenceSet interface


## -description


An unordered set of <a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a> interface pointers that represent references to parts to be signed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcSignaturePartReferenceSet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcSignaturePartReferenceSet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcSignaturePartReferenceSet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63162b37-0262-4d92-a14f-726fe4c87cc1">Create</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a> interface pointer that represents a reference to a part to be signed, and adds the new interface to the set.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22f69c35-d85c-46cc-bd1b-5ca4eada3a2f">Delete</a>
</td>
<td align="left" width="63%">

              Deletes a specified <a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a> interface pointer from the set.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b345fe9-55b3-447c-9b5b-64ab292ab734">GetEnumerator</a>
</td>
<td align="left" width="63%">

              Gets an enumerator of <a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a> interface pointers  in the set.
            

</td>
</tr>
</table> 


## -remarks



Only parts that can be represented by the <a href="https://msdn.microsoft.com/e6a40f30-03d1-4c93-a5e0-563b4c6588b4">IOpcPart</a> interface can be referenced by an <a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a> interface pointer. Relationships parts are referenced for signing  by a pointer to the <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface. To create an <b>IOpcSignatureRelationshipReference</b> interface pointer, call the  <a href="https://msdn.microsoft.com/c348ac25-f2b3-491d-b378-f0daf282b1ca">IOpcSignatureRelationshipReferenceSet::Create</a> method.

When an <a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a> interface pointer is created and added to the set, the reference it represents is saved when the package is saved.

When an <a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a> interface pointer is deleted from the set, the reference it represents is not saved when the package is saved.

To create an <b>IOpcSignaturePartReferenceSet</b> interface pointer, call the <a href="https://msdn.microsoft.com/60e657c3-41a3-4a05-a084-111429b1add9">IOpcSigningOptions::GetSignaturePartReferenceSet</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/89ea7243-54ee-487b-a58a-0721af9db8c3">IOpcSignatureRelationshipReferenceSet</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<a href="https://msdn.microsoft.com/f8401d12-da2e-4b35-b473-ebe3d1f91abd">OPC_CANONICALIZATION_METHOD</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

