---
UID: NF:msopc.IOpcRelationshipSelectorEnumerator.GetCurrent
title: IOpcRelationshipSelectorEnumerator::GetCurrent
author: windows-sdk-content
description: Gets the IOpcRelationshipSelector interface pointer at the current position of the enumerator.
old-location: opc\iopcrelationshipselectorenumerator_getcurrent.htm
old-project: OPC
ms.assetid: ffff6b7e-8e46-4be6-921f-b98e7d51a114
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: GetCurrent, GetCurrent method [Open Packaging Conventions], GetCurrent method [Open Packaging Conventions],IOpcRelationshipSelectorEnumerator interface, IOpcRelationshipSelectorEnumerator interface [Open Packaging Conventions],GetCurrent method, IOpcRelationshipSelectorEnumerator.GetCurrent, IOpcRelationshipSelectorEnumerator::GetCurrent, msopc/IOpcRelationshipSelectorEnumerator::GetCurrent, opc.iopcrelationshipselectorenumerator_getcurrent
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
 - IOpcRelationshipSelectorEnumerator.GetCurrent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IOpcRelationshipSelectorEnumerator::GetCurrent


## -description


Gets the <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a> interface pointer at the current position of the enumerator.


## -parameters




### -param relationshipSelector [out, retval]

An <a href="https://msdn.microsoft.com/077f37c3-76af-4b96-9e3a-9fd9b865d941">IOpcRelationshipSelector</a> interface pointer .


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code/value</th>
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
The <i>partReference</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_ENUM_COLLECTION_CHANGED</b></dt>
<dt>0x80510050</dt>
</dl>
</td>
<td width="60%">
The enumerator is invalid because the underlying set has changed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OPC_E_ENUM_INVALID_POSITION</b></dt>
<dt>0x80510053</dt>
</dl>
</td>
<td width="60%">
The enumerator cannot perform this operation from its current position.

</td>
</tr>
</table>
 




## -remarks




  		When an enumerator is created, the current position precedes the first pointer.

To set the current position to the first pointer of the enumerator, call the  <a href="https://msdn.microsoft.com/81918b97-0d10-4d7c-aaad-fc886d55e664">MoveNext</a>
          method after creating the enumerator.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/62069595-0d1e-44e5-b68d-2bb0c355c565">Core Packaging Interfaces</a>



<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/9c0bbc0d-d950-4929-9100-41a7f016a208">IOpcRelationshipSelectorEnumerator</a>



<a href="https://msdn.microsoft.com/cb23cbe2-764c-47e4-bd32-2791ddde9eee">IOpcRelationshipSelectorSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

