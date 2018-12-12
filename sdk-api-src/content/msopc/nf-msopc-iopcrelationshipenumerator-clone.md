---
UID: NF:msopc.IOpcRelationshipEnumerator.Clone
title: IOpcRelationshipEnumerator::Clone
author: windows-sdk-content
description: Creates a copy of the current enumerator and all its descendants.
old-location: opc\iopcrelationshipenumerator_clone.htm
tech.root: OPC
ms.assetid: 838f9486-be46-461f-b570-bc77003f1619
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Clone, Clone method [Open Packaging Conventions], Clone method [Open Packaging Conventions],IOpcRelationshipEnumerator interface, IOpcRelationshipEnumerator interface [Open Packaging Conventions],Clone method, IOpcRelationshipEnumerator.Clone, IOpcRelationshipEnumerator::Clone, msopc/IOpcRelationshipEnumerator::Clone, opc.iopcrelationshipenumerator_clone
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
req.idl: Opcobjectmodel.idl
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
 - IOpcRelationshipEnumerator.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpcRelationshipEnumerator::Clone


## -description


Creates a copy of the current enumerator and all its descendants.


## -parameters




### -param copy [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/8d8071cb-89ea-421e-9475-04a028317198">IOpcRelationshipEnumerator</a> interface of the new enumerator.


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
The <i>copy</i> parameter is <b>NULL</b>.

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
</table>
 




## -remarks



When an enumerator is created, the current position precedes the first pointer. To set the current position to the first pointer of the enumerator, call the  <a href="https://msdn.microsoft.com/d0733a11-0ba6-445f-8e3c-b62ad7b6b4bf">MoveNext</a>method after creating the enumerator.


#### Thread Safety

Packaging objects are not thread-safe.

For more information, see the <a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>.




## -see-also




<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/8d8071cb-89ea-421e-9475-04a028317198">IOpcRelationshipEnumerator</a>



<a href="https://msdn.microsoft.com/6259906d-820d-4b6e-bbeb-d9d044f2b35a">IOpcRelationshipSet</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/7ab1cc09-ce81-4f56-8adf-d8c95bf2c4cd">Packaging API Reference</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<b>Reference</b>
 

 

