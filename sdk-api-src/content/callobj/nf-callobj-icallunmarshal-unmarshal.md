---
UID: NF:callobj.ICallUnmarshal.Unmarshal
title: ICallUnmarshal::Unmarshal (callobj.h)
author: windows-sdk-content
description: Turns a marshaled packet of data back into an activation record that can then be invoked or manipulated in some other way.
old-location: com\icallunmarshal_unmarshal.htm
tech.root: com
ms.assetid: 15d04287-285d-43d9-ad55-3dc9c7ae192e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICallUnmarshal interface [COM],Unmarshal method, ICallUnmarshal.Unmarshal, ICallUnmarshal::Unmarshal, Unmarshal, Unmarshal method [COM], Unmarshal method [COM],ICallUnmarshal interface, _com_icallunmarshal_unmarshal, callobj/ICallUnmarshal::Unmarshal, com.icallunmarshal_unmarshal
ms.topic: method
req.header: callobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Callobj.idl
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
 - Callobj.h
api_name:
 - ICallUnmarshal.Unmarshal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

