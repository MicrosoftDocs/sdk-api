---
UID: NN:msopc.IOpcSignatureRelationshipReferenceEnumerator
title: IOpcSignatureRelationshipReferenceEnumerator
author: windows-sdk-content
description: A read-only enumerator of IOpcSignatureRelationshipReference interface pointers.
old-location: opc\iopcsignaturerelationshipreferenceenumerator.htm
old-project: OPC
ms.assetid: aa4c6e8b-1a1f-464b-885e-bee0976afafc
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IOpcSignatureRelationshipReferenceEnumerator, IOpcSignatureRelationshipReferenceEnumerator interface [Open Packaging Conventions], IOpcSignatureRelationshipReferenceEnumerator interface [Open Packaging Conventions],described, msopc/IOpcSignatureRelationshipReferenceEnumerator, opc.iopcsignaturerelationshipreferenceenumerator
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
req.idl: 
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
 - IOpcSignatureRelationshipReferenceEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcSignatureRelationshipReferenceEnumerator interface


## -description


A read-only enumerator of <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcSignatureRelationshipReferenceEnumerator</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcSignatureRelationshipReferenceEnumerator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcSignatureRelationshipReferenceEnumerator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the current <b>IOpcSignatureRelationshipReferenceEnumerator</b> interface pointer and all its descendants.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18aac7c9-db1a-4fc5-896e-7a02c12788f2">GetCurrent</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointer at the current position of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f004339-0cbf-4125-a09e-3b94ee22a0df">MoveNext</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the next <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c56f871f-50ca-4253-84db-0602459fc2fa">MovePrevious</a>
</td>
<td align="left" width="63%">
Moves the current position of the enumerator to the previous <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointer.

</td>
</tr>
</table> 


## -remarks



When an enumerator is created, the current position precedes the first pointer. To set the current position to the first pointer of the enumerator, call the  <a href="https://msdn.microsoft.com/6f004339-0cbf-4125-a09e-3b94ee22a0df">MoveNext</a>method after creating the enumerator.

Changes to the set will invalidate the enumerator and all subsequent calls to it will fail.

To get an <b>IOpcSignatureRelationshipReferenceEnumerator</b> interface pointer, call the <a href="https://msdn.microsoft.com/a574a935-f89a-445f-a793-d8dc2e116a48">IOpcSignatureRelationshipReferenceSet::GetEnumerator</a> or <a href="https://msdn.microsoft.com/ffb74828-1177-4c3d-8a8c-e40bb0c4cbf0">IOpcDigitalSignature::GetSignatureRelationshipReferenceEnumerator</a> method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/89ea7243-54ee-487b-a58a-0721af9db8c3">IOpcSignatureRelationshipReferenceSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

