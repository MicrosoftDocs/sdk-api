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

# CoGetCallerTID function


## -description


Returns a pointer to a <b>DWORD</b> that contains the apartment ID of the caller's thread.


## -parameters




### -param lpdwTID [out]

Receives the apartment ID of the caller's thread. For a single threaded apartment (STA), this is the current thread ID. For a multithreaded apartment (MTA), the value is 0.  For a neutral apartment (NA), the value is -1.


## -returns



This function can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_TRUE</b></dt>
</dl>
</td>
<td width="60%">
The caller's thread ID is set and the caller is in the same process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The caller's thread ID is set and the caller is in a different process.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller's thread ID was not set.

</td>
</tr>
</table>
 




## -remarks



If the caller is not running on the same computer, this function does not return the apartment ID and the return value is S_FALSE.

There is no guarantee that the information returned from this API is not tampered with, so do not use the ID that is returned to make security decisions. The ID can only be used for logging and diagnostic purposes.



