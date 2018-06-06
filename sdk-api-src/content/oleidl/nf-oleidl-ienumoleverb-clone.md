---
UID: NF:oleidl.IEnumOLEVERB.Clone
title: IEnumOLEVERB::Clone
author: windows-sdk-content
description: Creates a new enumerator that contains the same enumeration state as the current one.
old-location: com\ienumoleverb_clone.htm
old-project: com
ms.assetid: b93eafa0-c9c5-4d3f-a9a0-c5ca95df5b03
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: Clone, Clone method [COM], Clone method [COM],IEnumOLEVERB interface, IEnumOLEVERB interface [COM],Clone method, IEnumOLEVERB.Clone, IEnumOLEVERB::Clone, _ole_ienumoleverb_clone, com.ienumoleverb_clone, oleidl/IEnumOLEVERB::Clone
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IEnumOLEVERB.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IEnumOLEVERB::Clone


## -description


Creates a new enumerator that contains the same enumeration state as the current one.

This method makes it possible to record a particular point in the enumeration sequence and then return to that point at a later time. The caller must release this new enumerator separately from the first enumerator.


## -parameters




### -param ppenum [out]

A pointer to an <a href="https://msdn.microsoft.com/fc9b3474-6f56-4274-af7d-72e0920c0457">IEnumOLEVERB</a> pointer variable that receives the interface pointer to the enumeration object. If the method is unsuccessful, the value of this output variable is undefined.


## -returns



This method returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified enumerator is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available for this operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fc9b3474-6f56-4274-af7d-72e0920c0457">IEnumOLEVERB</a>
 

 

