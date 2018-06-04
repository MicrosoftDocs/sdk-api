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

# ICallFrame::Marshal


## -description


Marshals the call frame by turning its reachable data into a flat buffer without disturbing the frame.



## -parameters




### -param pmshlContext [in]

A pointer to the <a href="https://msdn.microsoft.com/4ecc4646-db3f-4d0e-9c45-b78a288156e1">CALLFRAME_MARSHALCONTEXT</a> structure containing context information about how marshalling is carried out.


### -param mshlflags [in]

Flag indicating whether the data to be marshaled is to be transmitted back to the client process â€” the normal case â€” or written to a global table, where it can be retrieved by multiple clients. The possible values are from the <a href="https://msdn.microsoft.com/42a482be-d4b8-4f2e-ae43-1d210cb44c7c">MSHLFLAGS</a> enumeration.


### -param pBuffer [in]

A pointer to the buffer into which the marshaled data is to be placed.


### -param cbBuffer [in]

The size of the buffer, in bytes.


### -param pcbBufferUsed [out]

Receives the size of the buffer that was actually used. This parameter is optional.


### -param pdataRep [out]

Receives the NDR data representation with which the data was marshaled. This parameter is optional. For more information, see <a href="https://msdn.microsoft.com/775a15df-8bcf-4c1b-a8b9-5c7c03106c09">IRpcChannelBuffer::GetBuffer</a>.


### -param prpcFlags [out]

Receives an RPC flag associated with the call. This parameter is optional. For more information, see <a href="https://msdn.microsoft.com/775a15df-8bcf-4c1b-a8b9-5c7c03106c09">IRpcChannelBuffer::GetBuffer</a>.


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
 




## -remarks



When marshalling the [In] versions of [in, out] parameters are present, and the [out] versions are undefined. When marshalling [out] parameters the values are valid.

If this method returns an error, the caller will not be able to clean it up. Resources such as memory transiently allocated during the attempted marshalling have been freed.




## -see-also




<a href="https://msdn.microsoft.com/56a75123-f402-4187-af13-d31f72a5f094">ICallFrame</a>
 

 

