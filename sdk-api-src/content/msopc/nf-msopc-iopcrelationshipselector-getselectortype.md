---
UID: NF:msopc.IOpcRelationshipSelector.GetSelectorType
title: IOpcRelationshipSelector::GetSelectorType
author: windows-driver-content
description: Gets a value that describes how relationships are selected to be referenced for signing.
old-location: opc\iopcrelationshipselector_getselectortype.htm
old-project: OPC
ms.assetid: 583f56e5-c374-4f79-badd-35eb5eecef70
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetSelectorType, GetSelectorType method [Open Packaging Conventions], GetSelectorType method [Open Packaging Conventions],IOpcRelationshipSelector interface, IOpcRelationshipSelector interface [Open Packaging Conventions],GetSelectorType method, IOpcRelationshipSelector.GetSelectorType, IOpcRelationshipSelector::GetSelectorType, msopc/IOpcRelationshipSelector::GetSelectorType, opc.iopcrelationshipselector_getselectortype
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
req.typenames: OPC_SIGNATURE_TIME_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msopc.h
api_name:
-	IOpcRelationshipSelector.GetSelectorType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcRelationshipSelector::GetSelectorType


## -description


Gets a value that describes how relationships are selected to be referenced for signing.


## -parameters




### -param selector [out, retval]

A value that describes which <a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a> interface property will be compared to the string returned by the <a href="https://msdn.microsoft.com/ac1f0347-9b89-4d8f-b0cb-14708e7a6e55">GetSelectionCriterion</a> method.


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
The <i>selector</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The following table shows how <a href="https://msdn.microsoft.com/5532aab1-850e-4de8-a470-c55fb4c2f8c4">OPC_RELATIONSHIP_SELECTOR</a> values map to the relationship type and relationship identifier properties.<table>
<tr>
<th>
<a href="https://msdn.microsoft.com/5532aab1-850e-4de8-a470-c55fb4c2f8c4">OPC_RELATIONSHIP_SELECTOR</a>  Value</th>
<th>Relationship Property</th>
<th>Description</th>
</tr>
<tr>
<td><b>OPC_RELATIONSHIP_SELECT_BY_TYPE</b></td>
<td>Relationship type</td>
<td>
Selects relationships that have a relationship type that matches <i>selectionCriterion</i> string.

</td>
</tr>
<tr>
<td><b>OPC_RELATIONSHIP_SELECT_BY_ID</b></td>
<td>Relationship identifier</td>
<td>
Selects relationships that have a relationship identifier that matches <i>selectionCriterion</i> string.

</td>
</tr>
</table>
 




#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a>



<a href="https://msdn.microsoft.com/9c0bbc0d-d950-4929-9100-41a7f016a208">IOpcRelationshipSelectorEnumerator</a>



<a href="https://msdn.microsoft.com/cb23cbe2-764c-47e4-bd32-2791ddde9eee">IOpcRelationshipSelectorSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

