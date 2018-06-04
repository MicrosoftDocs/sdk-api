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

# ClearCommError function


## -description


Retrieves information about a communications error and reports the current status of a communications device. The function is called when a communications error occurs, and it clears the device's error flag to enable additional input and output (I/O) operations.


## -parameters




### -param hFile [in]

A handle to the communications device. The 
<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function returns this handle.


### -param lpErrors [out, optional]

A pointer to a variable that receives a mask indicating the type of error. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CE_BREAK"></a><a id="ce_break"></a><dl>
<dt><b>CE_BREAK</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The hardware detected a break condition.

</td>
</tr>
<tr>
<td width="40%"><a id="CE_FRAME"></a><a id="ce_frame"></a><dl>
<dt><b>CE_FRAME</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The hardware detected a framing error.

</td>
</tr>
<tr>
<td width="40%"><a id="CE_OVERRUN"></a><a id="ce_overrun"></a><dl>
<dt><b>CE_OVERRUN</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
A character-buffer overrun has occurred. The next character is lost.

</td>
</tr>
<tr>
<td width="40%"><a id="CE_RXOVER"></a><a id="ce_rxover"></a><dl>
<dt><b>CE_RXOVER</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
An input buffer overflow has occurred. There is either no room in the input buffer, or a character was received after the end-of-file (EOF) character.

</td>
</tr>
<tr>
<td width="40%"><a id="CE_RXPARITY"></a><a id="ce_rxparity"></a><dl>
<dt><b>CE_RXPARITY</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The hardware detected a parity error.

</td>
</tr>
</table>
 

The following values are not supported:


### -param lpStat [out, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/dd54d040-1244-425f-a43e-9071d679c4ec">COMSTAT</a> structure in which the device's status information is returned. If this parameter is <b>NULL</b>, no status information is returned.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If a communications port has been set up with a <b>TRUE</b> value for the <b>fAbortOnError</b> member of the setup 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541431">DCB</a> structure, the communications software will terminate all read and write operations on the communications port when a communications error occurs. No new read or write operations will be accepted until the application acknowledges the communications error by calling the 
<b>ClearCommError</b> function.

The 
<b>ClearCommError</b> function fills the status buffer pointed to by the <i>lpStat</i> parameter with the current status of the communications device specified by the <i>hFile</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/dd54d040-1244-425f-a43e-9071d679c4ec">COMSTAT</a>



<a href="https://msdn.microsoft.com/9692242c-e209-4492-ab0b-333f09595597">ClearCommBreak</a>



<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541431">DCB</a>
 

 

