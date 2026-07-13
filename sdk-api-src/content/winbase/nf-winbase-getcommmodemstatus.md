---
UID: NF:winbase.GetCommModemStatus
title: GetCommModemStatus function (winbase.h)
description: Retrieves the modem control-register values.
helpviewer_keywords: ["GetCommModemStatus","GetCommModemStatus function","MS_CTS_ON","MS_DSR_ON","MS_RING_ON","MS_RLSD_ON","_win32_getcommmodemstatus","base.getcommmodemstatus","winbase/GetCommModemStatus"]
old-location: base\getcommmodemstatus.htm
tech.root: base
ms.assetid: 937bb623-d02d-452e-a8a2-21d9a6c5cac0
ms.date: 12/05/2018
ms.keywords: GetCommModemStatus, GetCommModemStatus function, MS_CTS_ON, MS_DSR_ON, MS_RING_ON, MS_RLSD_ON, _win32_getcommmodemstatus, base.getcommmodemstatus, winbase/GetCommModemStatus
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetCommModemStatus
 - winbase/GetCommModemStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-comm-l1-1-2.dll
 - api-ms-win-core-comm-l1-1-1.dll
 - Kernel32.dll
 - API-MS-Win-Core-comm-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetCommModemStatus
---

# GetCommModemStatus function


## -description

Retrieves the modem control-register values.

## -parameters

### -param hFile [in]

A handle to the communications device. The 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function returns this handle.

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
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>GetCommModemStatus</b> function is useful when you are using the 
<a href="/windows/desktop/api/winbase/nf-winbase-waitcommevent">WaitCommEvent</a> function to monitor the CTS, RLSD, DSR, or ring indicator signals. To detect when these signals change state, use 
<b>WaitCommEvent</b> and then use 
<b>GetCommModemStatus</b> to determine the state after a change occurs.

The function fails if the hardware does not support the control-register values.

## -see-also

<a href="/windows/desktop/DevIO/communications-functions">Communications Functions</a>



<a href="/windows/desktop/DevIO/communications-resources">Communications Resources</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-waitcommevent">WaitCommEvent</a>