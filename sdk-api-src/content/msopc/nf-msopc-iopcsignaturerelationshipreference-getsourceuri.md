---
UID: NF:msopc.IOpcSignatureRelationshipReference.GetSourceUri
title: IOpcSignatureRelationshipReference::GetSourceUri
author: windows-sdk-content
description: Gets the source URI of the relationships that are stored in the referenced&#160;Relationships part.
old-location: opc\iopcsignaturerelationshipreference_getsourceuri.htm
old-project: OPC
ms.assetid: d08cfbf0-0917-4ca4-85be-5ca62d7029d0
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetSourceUri, GetSourceUri method [Open Packaging Conventions], GetSourceUri method [Open Packaging Conventions],IOpcSignatureRelationshipReference interface, IOpcSignatureRelationshipReference interface [Open Packaging Conventions],GetSourceUri method, IOpcSignatureRelationshipReference.GetSourceUri, IOpcSignatureRelationshipReference::GetSourceUri, msopc/IOpcSignatureRelationshipReference::GetSourceUri, opc.iopcsignaturerelationshipreference_getsourceuri
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msopc.h
req.include-header: 
req.redist: 
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
 - IOpcSignatureRelationshipReference.GetSourceUri
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcSignatureRelationshipReference::GetSourceUri


## -description


Gets the  source URI of the relationships that are stored in the referenced Relationships part.


## -parameters




### -param sourceUri [out, retval]

A pointer to the source URI of the relationships that are stored in the referenced Relationships part.


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
The <i>sourceUri</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




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
 

 

