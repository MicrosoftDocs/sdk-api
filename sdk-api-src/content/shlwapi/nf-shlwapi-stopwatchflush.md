---
UID: NF:shlwapi.StopWatchFlush
title: StopWatchFlush function (shlwapi.h)
description: StopWatchFlush may be altered or unavailable.
helpviewer_keywords: ["StopWatchFlush","StopWatchFlush function [Windows Shell]","_win32_StopWatchFlush","shell.StopWatchFlush","shlwapi/StopWatchFlush"]
old-location: shell\StopWatchFlush.htm
tech.root: shell
ms.assetid: 52b79602-6e24-4d66-a400-5745149e744b
ms.date: 12/05/2018
ms.keywords: StopWatchFlush, StopWatchFlush function [Windows Shell], _win32_StopWatchFlush, shell.StopWatchFlush, shlwapi/StopWatchFlush
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
 - StopWatchFlush
 - shlwapi/StopWatchFlush
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
 - StopWatchFlush
---

# StopWatchFlush function


## -description

<p class="CCE_Message">[<b>StopWatchFlush</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Writes out performance statistics if performance logging is enabled.



## -returns

Type: <b>DWORD</b>

ERROR_SUCCESS on success, or an error code on failure. Possible error codes include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_DATA</b></dt>
</dl>
</td>
<td width="60%">
No performance logs were collected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
Performance logging is not enabled.

</td>
</tr>
</table>

## -remarks

The performance log is written to the shperf.log file in the Windows directory.  If message performance logs are enabled, the message performance log is written to the msgtrace.log file in the Windows directory. If you call <b>StopWatchFlush</b>, you must have permission to create and modify files in the Windows directory.

Calling <b>StopWatchFlush</b> clears the performance logs after writing them to the shperf.log file.

See the <a href="/windows/desktop/api/shlwapi/nf-shlwapi-stopwatchmode">StopWatchMode</a> function for a description of the information that is recorded in the performance log.
