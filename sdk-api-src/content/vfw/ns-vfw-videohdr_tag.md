---
UID: NS:vfw.videohdr_tag
title: videohdr_tag
author: windows-sdk-content
description: The VIDEOHDR structure is used by the capVideoStreamCallback function.
old-location: multimedia\videohdr.htm
tech.root: Multimedia
ms.assetid: 81e4dded-7ba1-40cf-bc16-20524b70a28d
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: "*LPVIDEOHDR, *PVIDEOHDR, LPVIDEOHDR, LPVIDEOHDR structure pointer [Windows Multimedia], PVIDEOHDR, PVIDEOHDR structure pointer [Windows Multimedia], VIDEOHDR, VIDEOHDR structure [Windows Multimedia], _win32_VIDEOHDR_str, multimedia.videohdr, vfw/LPVIDEOHDR, vfw/PVIDEOHDR, vfw/VIDEOHDR, videohdr_tag"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - VIDEOHDR
product: Windows
targetos: Windows
req.typenames: VIDEOHDR, *PVIDEOHDR, *LPVIDEOHDR
req.redist: 
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
 

 

