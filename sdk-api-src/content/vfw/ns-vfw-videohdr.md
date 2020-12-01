---
UID: NS:vfw.videohdr_tag
title: VIDEOHDR (vfw.h)
description: The VIDEOHDR structure is used by the capVideoStreamCallback function.
helpviewer_keywords: ["*LPVIDEOHDR","*PVIDEOHDR","LPVIDEOHDR","LPVIDEOHDR structure pointer [Windows Multimedia]","PVIDEOHDR","PVIDEOHDR structure pointer [Windows Multimedia]","VIDEOHDR","VIDEOHDR structure [Windows Multimedia]","_win32_VIDEOHDR_str","multimedia.videohdr","vfw/LPVIDEOHDR","vfw/PVIDEOHDR","vfw/VIDEOHDR"]
old-location: multimedia\videohdr.htm
tech.root: Multimedia
ms.assetid: 81e4dded-7ba1-40cf-bc16-20524b70a28d
ms.date: 12/05/2018
ms.keywords: '*LPVIDEOHDR, *PVIDEOHDR, LPVIDEOHDR, LPVIDEOHDR structure pointer [Windows Multimedia], PVIDEOHDR, PVIDEOHDR structure pointer [Windows Multimedia], VIDEOHDR, VIDEOHDR structure [Windows Multimedia], _win32_VIDEOHDR_str, multimedia.videohdr, vfw/LPVIDEOHDR, vfw/PVIDEOHDR, vfw/VIDEOHDR'
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
targetos: Windows
req.typenames: VIDEOHDR, *PVIDEOHDR, *LPVIDEOHDR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - videohdr_tag
 - vfw/videohdr_tag
 - PVIDEOHDR
 - vfw/PVIDEOHDR
 - VIDEOHDR
 - vfw/VIDEOHDR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - VIDEOHDR
---

# VIDEOHDR structure


## -description

The <b>VIDEOHDR</b> structure is used by the <a href="/windows/desktop/api/vfw/nc-vfw-capvideocallback">capVideoStreamCallback</a> function.

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

<a href="/windows/desktop/Multimedia/multimedia-timer-structures">Multimedia Timer Structures</a>



<a href="/windows/desktop/Multimedia/multimedia-timers">Multimedia Timers</a>



<a href="/windows/desktop/api/vfw/nc-vfw-capvideocallback">capVideoStreamCallback</a>