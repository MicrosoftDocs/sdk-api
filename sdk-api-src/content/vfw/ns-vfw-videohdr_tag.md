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

# videohdr_tag structure


## -description



The <b>VIDEOHDR</b> structure is used by the <a href="https://msdn.microsoft.com/e21d7563-0ca8-4777-9fb0-de7c1c4ae618">capVideoStreamCallback</a> function.




## -struct-fields




### -field lpData


            Pointer to locked data buffer.
          


### -field dwBufferLength


            Length of data buffer.
          


### -field dwBytesUsed


            Bytes actually used.
          


### -field dwTimeCaptured


            Milliseconds from start of stream.
          


### -field dwUser


            User-defined data.
          


### -field dwFlags

The flags are defined as follows.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>VHDR_DONE</td>
<td>Done bit</td>
</tr>
<tr>
<td>VHDR_PREPARED</td>
<td>Set if this header has been prepared</td>
</tr>
<tr>
<td>VHDR_INQUEUE</td>
<td>Reserved for driver</td>
</tr>
<tr>
<td>VHDR_KEYFRAME</td>
<td>Key Frame</td>
</tr>
</table>
 


### -field dwReserved


            Reserved for driver.
          


## -see-also




<a href="https://msdn.microsoft.com/202c27be-01d5-4381-b71a-7a3f4e4c7adf">Multimedia Timer Structures</a>



<a href="https://msdn.microsoft.com/25e0b313-64ff-4f30-ae0a-ac364ce3f0cf">Multimedia Timers</a>



<a href="https://msdn.microsoft.com/e21d7563-0ca8-4777-9fb0-de7c1c4ae618">capVideoStreamCallback</a>
 

 

