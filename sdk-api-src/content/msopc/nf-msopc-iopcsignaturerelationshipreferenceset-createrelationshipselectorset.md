---
UID: NF:msopc.IOpcSignatureRelationshipReferenceSet.CreateRelationshipSelectorSet
title: IOpcSignatureRelationshipReferenceSet::CreateRelationshipSelectorSet
author: windows-sdk-content
description: Creates an IOpcRelationshipSelectorSet interface pointer that is used as the selectorSet parameter value of the Create method.
old-location: opc\iopcsignaturerelationshipreferenceset_createrelationshipselectorset.htm
old-project: OPC
ms.assetid: 7b11f066-3e3a-4dd0-a938-853301bc6914
ms.author: windowssdkdev
ms.date: 03/15/2018
ms.keywords: CreateRelationshipSelectorSet, CreateRelationshipSelectorSet method [Open Packaging Conventions], CreateRelationshipSelectorSet method [Open Packaging Conventions],IOpcSignatureRelationshipReferenceSet interface, IOpcSignatureRelationshipReferenceSet interface [Open Packaging Conventions],CreateRelationshipSelectorSet method, IOpcSignatureRelationshipReferenceSet.CreateRelationshipSelectorSet, IOpcSignatureRelationshipReferenceSet::CreateRelationshipSelectorSet, msopc/IOpcSignatureRelationshipReferenceSet::CreateRelationshipSelectorSet, opc.iopcsignaturerelationshipreferenceset_createrelationshipselectorset
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
 - IOpcSignatureRelationshipReferenceSet.CreateRelationshipSelectorSet
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcSignatureRelationshipReferenceSet::CreateRelationshipSelectorSet


## -description


Creates an <a href="https://msdn.microsoft.com/cb23cbe2-764c-47e4-bd32-2791ddde9eee">IOpcRelationshipSelectorSet</a> interface pointer that is used as the <i>selectorSet</i> parameter value of the <a href="https://msdn.microsoft.com/c348ac25-f2b3-491d-b378-f0daf282b1ca">Create</a> method.


## -parameters




### -param selectorSet [out]

A new <a href="https://msdn.microsoft.com/cb23cbe2-764c-47e4-bd32-2791ddde9eee">IOpcRelationshipSelectorSet</a> interface pointer.


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
The <i>selectorSet</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



To select a subset of the relationships (which are stored in the Relationships part to be referenced) to be signed when the signature is generated, call the <a href="https://msdn.microsoft.com/c348ac25-f2b3-491d-b378-f0daf282b1ca">Create</a> method with the <i>relationshipSigningOption</i> parameter value set to <b>OPC_RELATIONSHIP_SIGN_USING_SELECTORS</b> and the <i>selectorSet</i> parameter value set to the <a href="https://msdn.microsoft.com/cb23cbe2-764c-47e4-bd32-2791ddde9eee">IOpcRelationshipSelectorSet</a> interface pointer created by this method.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/89ea7243-54ee-487b-a58a-0721af9db8c3">IOpcSignatureRelationshipReferenceSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

