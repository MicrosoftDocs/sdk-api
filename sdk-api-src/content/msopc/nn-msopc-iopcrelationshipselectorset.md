---
UID: NN:msopc.IOpcRelationshipSelectorSet
title: IOpcRelationshipSelectorSet
author: windows-sdk-content
description: An unordered set of IOpcRelationshipSelector interface pointers that represent the selection criteria that is used to identify relationships for signing.
old-location: opc\iopcrelationshipselectorset.htm
old-project: OPC
ms.assetid: cb23cbe2-764c-47e4-bd32-2791ddde9eee
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: IOpcRelationshipSelectorSet, IOpcRelationshipSelectorSet interface [Open Packaging Conventions], IOpcRelationshipSelectorSet interface [Open Packaging Conventions],described, msopc/IOpcRelationshipSelectorSet, opc.iopcrelationshipselectorset
ms.prod: windows
ms.technology: windows-sdk
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
-	IOpcRelationshipSelectorSet
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcRelationshipSelectorSet interface


## -description


An unordered set of <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a> interface pointers  that represent the selection criteria that is used to identify relationships for signing. The subset is selected from the relationships stored in a Relationships part.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOpcRelationshipSelectorSet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOpcRelationshipSelectorSet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOpcRelationshipSelectorSet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/801d1924-c75c-47b5-99fe-9d97ea8dfee1">Create</a>
</td>
<td align="left" width="63%">

              Creates an <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a> interface pointer to represent how a subset of relationships are selected to be signed, and adds the new pointer to the set.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a90757f7-bdb1-4cff-9a46-64ec953f2172">Delete</a>
</td>
<td align="left" width="63%">

              Deletes a specified <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a> interface pointer from the set.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c0a885a-8ee2-40fe-bbc6-d7036e4a4c40">GetEnumerator</a>
</td>
<td align="left" width="63%">

              Gets an enumerator of <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a> interface pointers in the set.
            

</td>
</tr>
</table> 


## -remarks



Use the methods of the <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a> interface pointers in the set to select relationships for signing.

To create an <b>IOpcRelationshipSelectorSet</b> interface pointer, call the <a href="https://msdn.microsoft.com/7b11f066-3e3a-4dd0-a938-853301bc6914">IOpcSignatureRelationshipReference::CreateRelationshipSelectorSet</a> method.

When an <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a> interface pointer is created and added to the set, the criterion it provides access to is saved when the package is saved.

When an <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a> interface pointer is deleted from the set, the criterion it provides access to is not saved when the package is saved.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/9c0bbc0d-d950-4929-9100-41a7f016a208">IOpcRelationshipSelectorEnumerator</a>



<a href="https://msdn.microsoft.com/24aebfff-6b4f-49cb-988f-670ffed7d815">IOpcSignatureRelationshipReference</a>



<a href="https://msdn.microsoft.com/5532aab1-850e-4de8-a470-c55fb4c2f8c4">OPC_RELATIONSHIP_SELECTOR</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/76455a88-81be-45d9-a682-2ba43038b43f">Packaging Digital Signature Interfaces</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

