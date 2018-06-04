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

# GetCommModemStatus function


## -description


Retrieves the modem control-register values.


## -parameters




### -param hFile [in]

A handle to the communications device. The 
<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function returns this handle.


### -param lpModemStat [out]

A pointer to a variable that receives the current state of the modem control-register values. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MS_CTS_ON"></a><a id="ms_cts_on"></a><dl>
<dt><b>MS_CTS_ON</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The CTS (clear-to-send) signal is on.

</td>
</tr>
<tr>
<td width="40%"><a id="MS_DSR_ON"></a><a id="ms_dsr_on"></a><dl>
<dt><b>MS_DSR_ON</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
The DSR (data-set-ready) signal is on.

</td>
</tr>
<tr>
<td width="40%"><a id="MS_RING_ON"></a><a id="ms_ring_on"></a><dl>
<dt><b>MS_RING_ON</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
The ring indicator signal is on.

</td>
</tr>
<tr>
<td width="40%"><a id="MS_RLSD_ON"></a><a id="ms_rlsd_on"></a><dl>
<dt><b>MS_RLSD_ON</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
The RLSD (receive-line-signal-detect) signal is on.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>GetCommModemStatus</b> function is useful when you are using the 
<a href="https://msdn.microsoft.com/79e955c0-8756-4d6f-bce6-49e8e44d0d3f">WaitCommEvent</a> function to monitor the CTS, RLSD, DSR, or ring indicator signals. To detect when these signals change state, use 
<b>WaitCommEvent</b> and then use 
<b>GetCommModemStatus</b> to determine the state after a change occurs.

The function fails if the hardware does not support the control-register values.




## -see-also




<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/79e955c0-8756-4d6f-bce6-49e8e44d0d3f">WaitCommEvent</a>
 

 

