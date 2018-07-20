---
UID: NF:winbase.GetCommMask
title: GetCommMask function
author: windows-sdk-content
description: Retrieves the value of the event mask for a specified communications device.
old-location: base\getcommmask.htm
old-project: devio
ms.assetid: 502aa563-c783-4a98-8596-74514a5b261e
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: EV_BREAK, EV_CTS, EV_DSR, EV_ERR, EV_EVENT1, EV_EVENT2, EV_PERR, EV_RING, EV_RLSD, EV_RX80FULL, EV_RXCHAR, EV_RXFLAG, EV_TXEMPTY, GetCommMask, GetCommMask function, _win32_getcommmask, base.getcommmask, winbase/GetCommMask
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - GetCommMask
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetCommMask function


## -description


Retrieves the value of the event mask for a specified communications device.


## -parameters




### -param hFile [in]

A handle to the communications device. The 
<a href="base.createfile">CreateFile</a> function returns this handle.


### -param lpEvtMask [out]

A pointer to the variable that receives a mask of events that are currently enabled. This parameter can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EV_BREAK"></a><a id="ev_break"></a><dl>
<dt><b>EV_BREAK</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
A break was detected on input.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_CTS"></a><a id="ev_cts"></a><dl>
<dt><b>EV_CTS</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The CTS (clear-to-send) signal changed state.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_DSR"></a><a id="ev_dsr"></a><dl>
<dt><b>EV_DSR</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The DSR (data-set-ready) signal changed state.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_ERR"></a><a id="ev_err"></a><dl>
<dt><b>EV_ERR</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
A line-status error occurred. Line-status errors are <b>CE_FRAME</b>, <b>CE_OVERRUN</b>, and <b>CE_RXPARITY</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_EVENT1"></a><a id="ev_event1"></a><dl>
<dt><b>EV_EVENT1</b></dt>
<dt>0x0800</dt>
</dl>
</td>
<td width="60%">
An event of the first provider-specific type occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_EVENT2"></a><a id="ev_event2"></a><dl>
<dt><b>EV_EVENT2</b></dt>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
An event of the second provider-specific type occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_PERR"></a><a id="ev_perr"></a><dl>
<dt><b>EV_PERR</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
A printer error occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_RING"></a><a id="ev_ring"></a><dl>
<dt><b>EV_RING</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
A ring indicator was detected.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_RLSD"></a><a id="ev_rlsd"></a><dl>
<dt><b>EV_RLSD</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
The RLSD (receive-line-signal-detect) signal changed state.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_RX80FULL"></a><a id="ev_rx80full"></a><dl>
<dt><b>EV_RX80FULL</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
The receive buffer is 80 percent full.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_RXCHAR"></a><a id="ev_rxchar"></a><dl>
<dt><b>EV_RXCHAR</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
A character was received and placed in the input buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_RXFLAG"></a><a id="ev_rxflag"></a><dl>
<dt><b>EV_RXFLAG</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The event character was received and placed in the input buffer. The event character is specified in the device's 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff541431">DCB</a> structure, which is applied to a serial port by using the 
<a href="https://msdn.microsoft.com/a9296514-4789-4830-ba68-84a16ac7fc47">SetCommState</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="EV_TXEMPTY"></a><a id="ev_txempty"></a><dl>
<dt><b>EV_TXEMPTY</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The last character in the output buffer was sent.

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>GetCommMask</b> function uses a mask variable to indicate the set of events that can be monitored for a particular communications resource. A handle to the communications resource can be specified in a call to the 
<a href="https://msdn.microsoft.com/79e955c0-8756-4d6f-bce6-49e8e44d0d3f">WaitCommEvent</a> function, which waits for one of the events to occur. To modify the event mask of a communications resource, use the 
<a href="https://msdn.microsoft.com/77c86b02-7f98-439b-9072-d5fc3ef421a1">SetCommMask</a> function.




## -see-also




<a href="https://msdn.microsoft.com/ba7d1a9e-6906-4923-a8eb-db58050ba699">Communications Functions</a>



<a href="https://msdn.microsoft.com/7faf7d55-e30f-4be2-917b-e057265b81b2">Communications Resources</a>



<a href="base.createfile">CreateFile</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541431">DCB</a>



<a href="https://msdn.microsoft.com/77c86b02-7f98-439b-9072-d5fc3ef421a1">SetCommMask</a>



<a href="https://msdn.microsoft.com/79e955c0-8756-4d6f-bce6-49e8e44d0d3f">WaitCommEvent</a>
 

 

