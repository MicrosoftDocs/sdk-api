---
UID: NF:vfw.MCIWndGetTimeFormat
title: MCIWndGetTimeFormat macro
author: windows-sdk-content
description: The MCIWndGetTimeFormat macro retrieves the current time format of an MCI device in two forms:\_as a numerical value and as a string. You can use this macro or explicitly send the MCIWNDM_GETTIMEFORMAT message.
old-location: multimedia\mciwndgettimeformat.htm
old-project: Multimedia
ms.assetid: 91d212b5-1c30-4470-9f94-f704ed53a615
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: MCIWndGetTimeFormat, MCIWndGetTimeFormat macro [Windows Multimedia], _win32_MCIWndGetTimeFormat, multimedia.mciwndgettimeformat, vfw/MCIWndGetTimeFormat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - MCIWndGetTimeFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# MCIWndGetTimeFormat macro


## -description



The <b>MCIWndGetTimeFormat</b> macro retrieves the current time format of an MCI device in two forms: as a numerical value and as a string. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/01844872-5444-4f3b-92a3-64f80b94d3a0">MCIWNDM_GETTIMEFORMAT</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lp

Pointer to a buffer to contain the null-terminated string form of the time format. 


### -param len

Size, in bytes, of the buffer. 


## -remarks



If the time format string is longer than the return buffer, MCIWnd truncates the string.

An MCI device can support one or more of the following time formats:

<table>
<tr>
<th>
              Time format
            </th>
<th>
              MCI constant
            </th>
</tr>
<tr>
<td>Bytes</td>
<td>MCI_FORMAT_BYTES</td>
</tr>
<tr>
<td>Frames</td>
<td>MCI_FORMAT_FRAMES</td>
</tr>
<tr>
<td>Hours, minutes, seconds</td>
<td>MCI_FORMAT_HMS</td>
</tr>
<tr>
<td>Milliseconds</td>
<td>MCI_FORMAT_MILLISECONDS</td>
</tr>
<tr>
<td>Minutes, seconds, frames</td>
<td>MCI_FORMAT_MSF</td>
</tr>
<tr>
<td>Samples</td>
<td>MCI_FORMAT_SAMPLES</td>
</tr>
<tr>
<td>SMPTE 24</td>
<td>MCI_FORMAT_SMPTE_24</td>
</tr>
<tr>
<td>SMPTE 25</td>
<td>MCI_FORMAT_SMPTE_25</td>
</tr>
<tr>
<td>SMPTE 30 drop</td>
<td>MCI_FORMAT_SMPTE_30DROP</td>
</tr>
<tr>
<td>SMPTE 30 (non-drop)</td>
<td>MCI_FORMAT_SMPTE_30</td>
</tr>
<tr>
<td>Tracks, minutes, seconds, frames</td>
<td>MCI_FORMAT_TMSF</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/01844872-5444-4f3b-92a3-64f80b94d3a0">MCIWNDM_GETTIMEFORMAT</a>
 

 

