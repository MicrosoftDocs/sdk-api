---
UID: NF:msopc.IOpcSigningOptions.GetSignatureRelationshipReferenceSet
title: IOpcSigningOptions::GetSignatureRelationshipReferenceSet
author: windows-driver-content
description: Gets an IOpcSignatureRelationshipReferenceSet interface pointer.
old-location: opc\iopcsigningoptions_getsignaturerelationshipreferenceset.htm
old-project: OPC
ms.assetid: f89327d2-63ff-4b14-bde0-8fdf65f73e37
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetSignatureRelationshipReferenceSet, GetSignatureRelationshipReferenceSet method [Open Packaging Conventions], GetSignatureRelationshipReferenceSet method [Open Packaging Conventions],IOpcSigningOptions interface, IOpcSigningOptions interface [Open Packaging Conventions],GetSignatureRelationshipReferenceSet method, IOpcSigningOptions.GetSignatureRelationshipReferenceSet, IOpcSigningOptions::GetSignatureRelationshipReferenceSet, msopc/IOpcSigningOptions::GetSignatureRelationshipReferenceSet, opc.iopcsigningoptions_getsignaturerelationshipreferenceset
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IOpcSigningOptions.GetSignatureRelationshipReferenceSet
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IOpcSigningOptions::GetSignatureRelationshipReferenceSet


## -description


Gets an <a href="https://msdn.microsoft.com/89ea7243-54ee-487b-a58a-0721af9db8c3">IOpcSignatureRelationshipReferenceSet</a> interface pointer.


## -parameters




### -param relationshipReferenceSet [out, retval]

An <a href="https://msdn.microsoft.com/89ea7243-54ee-487b-a58a-0721af9db8c3">IOpcSignatureRelationshipReferenceSet</a> interface pointer.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>relationshipReferenceSet</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method gets an <a href="https://msdn.microsoft.com/89ea7243-54ee-487b-a58a-0721af9db8c3">IOpcSignatureRelationshipReferenceSet</a> interface pointer that provides methods enabling the creation and deletion of the <a href="https://msdn.microsoft.com/b4bbf854-96b4-412b-a22d-c810423a3752">IOpcSignaturePartReference</a> interface pointers in the set. The <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointers represent references to Relationships parts that contain relationships to be signed.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

