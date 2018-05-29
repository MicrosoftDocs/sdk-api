---
UID: NF:msopc.IOpcSignatureRelationshipReference.GetDigestValue
title: IOpcSignatureRelationshipReference::GetDigestValue
author: windows-sdk-content
description: Gets the digest value calculated for the selected relationships when they are signed.
old-location: opc\iopcsignaturerelationshipreference_getdigestvalue.htm
old-project: OPC
ms.assetid: 3c1f3e73-45fc-4325-bc7a-db9241385c4e
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: GetDigestValue, GetDigestValue method [Open Packaging Conventions], GetDigestValue method [Open Packaging Conventions],IOpcSignatureRelationshipReference interface, IOpcSignatureRelationshipReference interface [Open Packaging Conventions],GetDigestValue method, IOpcSignatureRelationshipReference.GetDigestValue, IOpcSignatureRelationshipReference::GetDigestValue, msopc/IOpcSignatureRelationshipReference::GetDigestValue, opc.iopcsignaturerelationshipreference_getdigestvalue
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msopc.h
api_name:
-	IOpcSignatureRelationshipReference.GetDigestValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcSignatureRelationshipReference::GetDigestValue


## -description


Gets the digest value calculated for the selected relationships when they are signed.


## -parameters




### -param digestValue [out]

A pointer to a buffer that contains the digest value calculated using the specified digest method; the method is applied to the relationship markup of the selected relationships when they are signed.


### -param count [out]

The size of the <i>digestValue</i> buffer.

If the selected relationships have not been signed yet, <i>count</i> is 0.


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
 At least one of the <i>digestValue</i>, and <i>count</i> parameters is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method allocates memory used by the buffer returned in <i>digestValue</i>.  If the method succeeds, call the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function to free the memory.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

