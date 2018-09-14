---
UID: NF:msopc.IOpcDigitalSignature.GetSignatureRelationshipReferenceEnumerator
title: IOpcDigitalSignature::GetSignatureRelationshipReferenceEnumerator
author: windows-sdk-content
description: Gets an enumerator of IOpcSignatureRelationshipReference interface pointers, which represent references to relationships that have been signed.
old-location: opc\iopcdigitalsignature_getsignaturerelationshipreferenceenumerator.htm
tech.root: OPC
ms.assetid: ffb74828-1177-4c3d-8a8c-e40bb0c4cbf0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetSignatureRelationshipReferenceEnumerator, GetSignatureRelationshipReferenceEnumerator method [Open Packaging Conventions], GetSignatureRelationshipReferenceEnumerator method [Open Packaging Conventions],IOpcDigitalSignature interface, IOpcDigitalSignature interface [Open Packaging Conventions],GetSignatureRelationshipReferenceEnumerator method, IOpcDigitalSignature.GetSignatureRelationshipReferenceEnumerator, IOpcDigitalSignature::GetSignatureRelationshipReferenceEnumerator, msopc/IOpcDigitalSignature::GetSignatureRelationshipReferenceEnumerator, opc.iopcdigitalsignature_getsignaturerelationshipreferenceenumerator
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
 - IOpcDigitalSignature.GetSignatureRelationshipReferenceEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcDigitalSignature::GetSignatureRelationshipReferenceEnumerator


## -description


Gets an enumerator of <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointers, which represent references to relationships that have been signed.


## -parameters




### -param relationshipReferenceEnumerator [out, retval]

A pointer to an enumerator of <a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a> interface pointers, which represent references to relationships that have been signed.


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
The <i>relationshipReferenceEnumerator</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/aa4c6e8b-1a1f-464b-885e-bee0976afafc">IOpcSignatureRelationshipReferenceEnumerator</a>



<a href="https://msdn.microsoft.com/89ea7243-54ee-487b-a58a-0721af9db8c3">IOpcSignatureRelationshipReferenceSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

