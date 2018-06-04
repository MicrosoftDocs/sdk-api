---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ICallFrame::GetMarshalSizeMax


## -description


Retrieves an upper bound on the number of bytes needed to marshal the call frame.

Usually an interface proxy calls this method to learn how big a buffer is needed, allocates the buffer, and then calls the <a href="https://msdn.microsoft.com/cab40c31-1f89-4da9-a1e0-ef946b34665c">Marshal</a> method to carry out the marshalling.


## -parameters




### -param pmshlContext [in]

A pointer to the <a href="https://msdn.microsoft.com/4ecc4646-db3f-4d0e-9c45-b78a288156e1">CALLFRAME_MARSHALCONTEXT</a> structure containing context information about how marshalling is carried out.


### -param mshlflags [in]

Indicates whether the data to be marshaled is to be transmitted back to the client process â€” the normal case â€” or written to a global table, where it can be retrieved by multiple clients. For a list of values, see the <a href="https://msdn.microsoft.com/42a482be-d4b8-4f2e-ae43-1d210cb44c7c">MSHLFLAGS</a> enumeration.


### -param pcbBufferNeeded [out]

A pointer to the size of the buffer, in bytes, that will be needed to marshal the call frame.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>
 

 

