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

# INetwork::GetTimeCreatedAndConnected


## -description


The <b>GetTimeCreatedAndConnected</b> method returns the local date and time when the network was created and connected.


## -parameters




### -param pdwLowDateTimeCreated [out]

Pointer to a datetime when  the network was created. Specifically, it contains the  low DWORD of <b>FILETIME.dwLowDateTime</b>.


### -param pdwHighDateTimeCreated [out]

Pointer to a datetime when  the network was created. Specifically, it contains the  high DWORD of <b>FILETIME.dwLowDateTime</b>.


### -param pdwLowDateTimeConnected [out]

Pointer to a datetime when the network was last connected to. Specifically, it contains the  low DWORD of <b>FILETIME.dwLowDateTime</b>.


### -param pdwHighDateTimeConnected [out]

Pointer to a datetime when the network was last connected to. Specifically, it contains the  high DWORD of <b>FILETIME.dwLowDateTime</b>.


## -returns



Returns S_OK if the method succeeds. Otherwise, the method returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The pointer passed is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6d483058-f7c4-4a6c-a1a8-816c2fab9994">INetwork</a>
 

 

