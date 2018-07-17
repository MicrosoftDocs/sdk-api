---
UID: NF:winbase.GetCommModemStatus
title: GetCommModemStatus function
author: windows-sdk-content
description: Retrieves the modem control-register values.
old-location: base\getcommmodemstatus.htm
old-project: DevIO
ms.assetid: 937bb623-d02d-452e-a8a2-21d9a6c5cac0
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetCommModemStatus, GetCommModemStatus function, MS_CTS_ON, MS_DSR_ON, MS_RING_ON, MS_RLSD_ON, _win32_getcommmodemstatus, base.getcommmodemstatus, winbase/GetCommModemStatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-comm-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetCommModemStatus
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetCommModemStatus function


## -description


Retrieves the modem control-register values.


## -parameters




### -param hFile [in]

A handle to the communications device. The 
<a href="base.createfile">CreateFile</a> function returns this handle.


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



<a href="base.createfile">CreateFile</a>



<a href="https://msdn.microsoft.com/79e955c0-8756-4d6f-bce6-49e8e44d0d3f">WaitCommEvent</a>
 

 

