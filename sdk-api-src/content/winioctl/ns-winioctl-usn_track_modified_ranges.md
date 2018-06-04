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

# USN_TRACK_MODIFIED_RANGES structure


## -description


Contains information on range tracking parameters for an update sequence number (USN) change journal using the <a href="https://msdn.microsoft.com/258E16B2-B6E8-44BB-8073-B1BEDD4FA86A">FSCTL_USN_TRACK_MODIFIED_RANGES</a> control code.


## -struct-fields




### -field Flags

Indicates enabling range tracking.

<table>
<tr>
<td>Value</td>
<td>Description</td>
</tr>
<tr>
<td>FLAG_USN_TRACK_MODIFIED_RANGES_ENABLE 
0x00000001 
</td>
<td>This flag is mandatory with <a href="https://msdn.microsoft.com/258E16B2-B6E8-44BB-8073-B1BEDD4FA86A">FSCTL_USN_TRACK_MODIFIED_RANGES</a> and is used to enable range tracking on the volume.</td>
</tr>
</table>
 


### -field Unused

Reserved.


### -field ChunkSize

Chunk size for tracking ranges. A single byte modification will be reflected as the whole chunk being modified.


### -field FileSizeThreshold

File size threshold to start outputting <a href="https://msdn.microsoft.com/2636D1A1-6FD1-4F84-954C-499DCCE6E390">USN_RECORD_V4</a> record(s) for modified file, i.e. if the modified file size is less than this threshold, then no <b>USN_RECORD_V4</b> record will be output. 


## -remarks



Once range tracking is enabled for a given volume it cannot be disabled except by deleting the USN Journal and recreating it.




## -see-also




<a href="https://msdn.microsoft.com/258E16B2-B6E8-44BB-8073-B1BEDD4FA86A">FSCTL_USN_TRACK_MODIFIED_RANGES</a>
 

 

