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
 

 

