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

# ICallUnmarshal::Unmarshal


## -description


Turns a marshaled packet of data back into an activation record that can then be invoked or manipulated in some other way.


## -parameters




### -param iMethod [in]

The method number. If this parameter is -1, the method number will be determined from the data to be unmarshaled.


### -param pBuffer [in]

A pointer to the buffer from which the activation record is to be created.


### -param cbBuffer [in]

The size of the buffer, in bytes.


### -param fForceBufferCopy [in]

Indicates whether the buffer should be copied and retained (nonzero) or the buffer will remain valid (zero).


### -param dataRep [in]

The data representation with which the data was marshaled.


### -param pcontext [in]

A pointer to a <a href="https://msdn.microsoft.com/4ecc4646-db3f-4d0e-9c45-b78a288156e1">CALLFRAME_MARSHALCONTEXT</a> structure that contains information about the context in which unmarshaling is to be carried out.


### -param pcbUnmarshalled [out]

A pointer to the number of bytes that were successfully unmarshaled.


### -param ppFrame [out]

A call frame bound to the umarshaled invocation.


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




<a href="https://msdn.microsoft.com/66de8d71-c27c-41bd-a741-02de5c779290">ICallUnmarshal</a>
 

 

