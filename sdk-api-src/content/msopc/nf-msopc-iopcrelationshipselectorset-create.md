---
UID: NF:msopc.IOpcRelationshipSelectorSet.Create
title: IOpcRelationshipSelectorSet::Create
author: windows-sdk-content
description: Creates an IOpcRelationshipSelector interface pointer to represent how a subset of relationships are selected to be signed, and adds the new pointer to the set.
old-location: opc\iopcrelationshipselectorset_create.htm
old-project: OPC
ms.assetid: 801d1924-c75c-47b5-99fe-9d97ea8dfee1
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: Create, Create method [Open Packaging Conventions], Create method [Open Packaging Conventions],IOpcRelationshipSelectorSet interface, IOpcRelationshipSelectorSet interface [Open Packaging Conventions],Create method, IOpcRelationshipSelectorSet.Create, IOpcRelationshipSelectorSet::Create, msopc/IOpcRelationshipSelectorSet::Create, opc.iopcrelationshipselectorset_create
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
-	IOpcRelationshipSelectorSet.Create
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcRelationshipSelectorSet::Create


## -description


Creates an <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a> interface pointer to represent how a subset of relationships are selected to be signed, and adds the new pointer to the set.


## -parameters




### -param selector [in]

A value that describes how to interpret the  string that is passed in <i>selectionCriterion</i>.


### -param selectionCriterion [in]

A string that is interpreted to yield a criterion.


### -param relationshipSelector [out, retval]

A new <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a> interface pointer that represents how relationships are selected from a Relationships part.

This parameter can be <b>NULL</b> if a pointer to the  new interface is not needed.


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
The value passed in the <i>selector</i> parameter is not a valid <a href="https://msdn.microsoft.com/5532aab1-850e-4de8-a470-c55fb4c2f8c4">OPC_RELATIONSHIP_SELECTOR</a> enumeration value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>partUri</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Use the methods of the <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a> interface pointers in the set to select relationships for signing.

When an <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a> interface pointer is created and added to the set, the criterion it provides access to is saved when the package is saved.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/cb23cbe2-764c-47e4-bd32-2791ddde9eee">IOpcRelationshipSelectorSet</a>



<a href="https://msdn.microsoft.com/5532aab1-850e-4de8-a470-c55fb4c2f8c4">OPC_RELATIONSHIP_SELECTOR</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

