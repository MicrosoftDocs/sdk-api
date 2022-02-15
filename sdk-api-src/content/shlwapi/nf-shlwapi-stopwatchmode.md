---
UID: NF:shlwapi.StopWatchMode
title: StopWatchMode function (shlwapi.h)
description: StopWatchMode may be altered or unavailable.
helpviewer_keywords: ["StopWatchMode","StopWatchMode function [Windows Shell]","_win32_StopWatchMode","shell.StopWatchMode","shlwapi/StopWatchMode"]
old-location: shell\StopWatchMode.htm
tech.root: shell
ms.assetid: 3db69040-0720-41a3-ba88-db885a2685aa
ms.date: 12/05/2018
ms.keywords: StopWatchMode, StopWatchMode function [Windows Shell], _win32_StopWatchMode, shell.StopWatchMode, shlwapi/StopWatchMode
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - StopWatchMode
 - shlwapi/StopWatchMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - StopWatchMode
---

# StopWatchMode function


## -description

<p class="CCE_Message">[<b>StopWatchMode</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Retrieves a value that indicates which performance information is being logged.



## -returns

Type: <b>DWORD</b>

The current stopwatch mode. If performance information is not being logged, then the stopwatch mode is zero. Otherwise, it consists of one or more of the following flags.

<table class="clsStd">
<tr>
<th>Flag</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>SPMODE_SHELL</td>
<td>0x00000001</td>
<td>Logs selected Windows Explorer actions.</td>
</tr>
<tr>
<td>SPMODE_DEBUGOUT</td>
<td>0x00000002</td>
<td>Has no effect.</td>
</tr>
<tr>
<td>SPMODE_TEST</td>
<td>0x00000004</td>
<td>Has no effect.</td>
</tr>
<tr>
<td>SPMODE_BROWSER</td>
<td>0x00000008</td>
<td>Logs selected activities of the Windows Explorer or Internet Explorer browser frame. This flag cannot be combined with SPMODE_EVENTTRACE.</td>
</tr>
<tr>
<td>SPMODE_FLUSH</td>
<td>0x00000010</td>
<td>Has no effect.</td>
</tr>
<tr>
<td>SPMODE_EVENT</td>
<td>0x00000020</td>
<td>Has no effect.</td>
</tr>
<tr>
<td>SPMODE_MSVM</td>
<td>0x00000040</td>
<td>Logs selected times for initializing the Microsoft VM.</td>
</tr>
<tr>
<td>SPMODE_FORMATTEXT</td>
<td>0x00000080</td>
<td>
Windows 2000: Indicates in the log which entries affect the browser frame.

Windows XP: Has no effect.

</td>
</tr>
<tr>
<td>SPMODE_PROFILE</td>
<td>0x00000100</td>
<td>Has no effect.</td>
</tr>
<tr>
<td>SPMODE_DEBUGBREAK</td>
<td>0x00000200</td>
<td>Breaks into the debugger after each log entry is created. If there is no debugger available, the program halts with a STATUS_BREAKPOINT exception.</td>
</tr>
<tr>
<td>SPMODE_MSGTRACE</td>
<td>0x00000400</td>
<td>Enables message performance logs.</td>
</tr>
<tr>
<td>SPMODE_PERFTAGS</td>
<td>0x00000800</td>
<td>Has no effect.</td>
</tr>
<tr>
<td>SPMODE_MEMWATCH</td>
<td>0x00001000</td>
<td>Has no effect.</td>
</tr>
<tr>
<td>SPMODE_DBMON</td>
<td>0x00002000</td>
<td>Has no effect.</td>
</tr>
<tr>
<td>SPMODE_MULTISTOP</td>
<td>0x00004000</td>
<td>Logs all "stop" operations even if there is only one matching "start".</td>
</tr>
<tr>
<td>SPMODE_EVENTTRACE</td>
<td>0x00008000</td>
<td>Logs selected activities of the MSHTML rendering engine. This flag cannot be combined with SPMODE_BROWSER.</td>
</tr>
</table>

## -remarks

To enable performance logging, set the following REG_DWORD registry value. You should restart your computer after setting this value, to ensure that the change has taken effect.




<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>Explorer</b>
                  <b>Performance</b>
                     <b>Mode</b></pre>


The information in the performance log is intended for internal measurement purposes and the exact contents change regularly. Performance logging in its current form is subject to change in the future.

Enabling performance logging degrades performance slightly.

<div class="alert"><b>Note</b>  When using Windows XP with Service Pack 2 (SP2) and later, performance data is not collected for a process until that process calls the <b>StopWatchMode</b> function for the first time, even if the above registry value has been set to a nonzero value.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-stopwatchflush">StopWatchFlush</a>
