---
UID: NF:msopc.IOpcRelationshipSelector.GetSelectionCriterion
title: IOpcRelationshipSelector::GetSelectionCriterion
author: windows-sdk-content
description: Gets a string that is used to select relationships to be referenced for signing.
old-location: opc\iopcrelationshipselector_getselectioncriterion.htm
tech.root: OPC
ms.assetid: ac1f0347-9b89-4d8f-b0cb-14708e7a6e55
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetSelectionCriterion, GetSelectionCriterion method [Open Packaging Conventions], GetSelectionCriterion method [Open Packaging Conventions],IOpcRelationshipSelector interface, IOpcRelationshipSelector interface [Open Packaging Conventions],GetSelectionCriterion method, IOpcRelationshipSelector.GetSelectionCriterion, IOpcRelationshipSelector::GetSelectionCriterion, msopc/IOpcRelationshipSelector::GetSelectionCriterion, opc.iopcrelationshipselector_getselectioncriterion
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
 - IOpcRelationshipSelector.GetSelectionCriterion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcRelationshipSelector::GetSelectionCriterion


## -description


Gets a string that is used to select relationships to be referenced for signing.


## -parameters




### -param selectionCriterion [out, retval]

A string used to select relationships  to be referenced for signing.


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
The <i>selectionCriterion</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method allocates memory used by the string returned in <i>selectionCriterion</i>.  If the method succeeds, call the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function to free the memory.

Use the <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a> interface methods to select relationships for signing. A relationship is selected if its type or identifier matches the string that is retrieved by calling the <b>GetSelectionCriterion</b> method. This string is either a relationship type or a relationship identifier.  Call the <a href="https://msdn.microsoft.com/583f56e5-c374-4f79-badd-35eb5eecef70">GetSelectorType</a> method to get an <a href="https://msdn.microsoft.com/5532aab1-850e-4de8-a470-c55fb4c2f8c4">OPC_RELATIONSHIP_SELECTOR</a> value to determine whether the string is a relationship type or an identifier. To access these relationship properties, call the <a href="https://msdn.microsoft.com/da832c8e-99e1-452a-90eb-97580f00f003">IOpcRelationship::GetRelationshipType</a> and <a href="https://msdn.microsoft.com/8646d592-d568-4b82-80f3-2673cd0d2721">IOpcRelationship::GetId</a> methods.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/d81f6569-6c95-4bb7-9d1d-51e10701b970">Digital Signatures Overview</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/eb3619bb-470f-41bd-a231-d63df70592c2">IOpcRelationship</a>



<a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a>



<a href="https://msdn.microsoft.com/9c0bbc0d-d950-4929-9100-41a7f016a208">IOpcRelationshipSelectorEnumerator</a>



<a href="https://msdn.microsoft.com/cb23cbe2-764c-47e4-bd32-2791ddde9eee">IOpcRelationshipSelectorSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

