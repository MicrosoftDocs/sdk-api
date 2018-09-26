---
UID: NF:objidl.IEnumFORMATETC.Clone
title: IEnumFORMATETC::Clone
author: windows-sdk-content
description: Creates a new enumerator that contains the same enumeration state as the current one.
old-location: com\ienumformatetc_clone.htm
tech.root: com
ms.assetid: 637c3299-816f-4f3c-9758-b3200b5cf153
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: Clone, Clone method [COM], Clone method [COM],IEnumFORMATETC interface, IEnumFORMATETC interface [COM],Clone method, IEnumFORMATETC.Clone, IEnumFORMATETC::Clone, _ole_ienumformatetc_clone, com.ienumformatetc_clone, objidl/IEnumFORMATETC::Clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - ObjIdl.h
api_name:
 - IEnumFORMATETC.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumFORMATETC::Clone


## -description


Creates a new enumerator that contains the same enumeration state as the current one.

This method makes it possible to record a particular point in the enumeration sequence and then return to that point at a later time. The caller must release this new enumerator separately from the first enumerator.


## -parameters




### -param ppenum [out]

Address of an <a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a> pointer variable that receives the interface pointer to the enumeration object. If the method is unsuccessful, the value of this output variable is undefined.


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




<a href="https://msdn.microsoft.com/4d180fdd-2d58-4d26-9242-6552dda0d3e6">IEnumFORMATETC</a>
 

 

