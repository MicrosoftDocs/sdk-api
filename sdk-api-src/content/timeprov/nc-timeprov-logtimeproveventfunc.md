---
UID: NC:timeprov.LogTimeProvEventFunc
title: LogTimeProvEventFunc (timeprov.h)
description: Logs a time provider event in the event log.
helpviewer_keywords: ["Error","Information","LogTimeProvEventFunc","LogTimeProvEventFunc callback","LogTimeProvEventFunc callback function","Warning","_win32_logtimeprovevent","base.logtimeprovevent","timeprov/LogTimeProvEventFunc"]
old-location: base\logtimeprovevent.htm
tech.root: winprog
ms.assetid: ddaea389-3f58-4011-bcf8-c60546d1bce1
ms.date: 12/05/2018
ms.keywords: Error, Information, LogTimeProvEventFunc, LogTimeProvEventFunc callback, LogTimeProvEventFunc callback function, Warning, _win32_logtimeprovevent, base.logtimeprovevent, timeprov/LogTimeProvEventFunc
req.header: timeprov.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LogTimeProvEventFunc
 - timeprov/LogTimeProvEventFunc
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Timeprov.h
api_name:
 - LogTimeProvEventFunc
---

# LogTimeProvEventFunc callback function


## -description

Logs a time provider event in the event log.

## -parameters

### -param wType [in]

The event type. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Error"></a><a id="error"></a><a id="ERROR"></a><dl>
<dt><b>Error</b></dt>
</dl>
</td>
<td width="60%">
Indicates a significant problem.

</td>
</tr>
<tr>
<td width="40%"><a id="Information"></a><a id="information"></a><a id="INFORMATION"></a><dl>
<dt><b>Information</b></dt>
</dl>
</td>
<td width="60%">
Provides information about a successful operation.

</td>
</tr>
<tr>
<td width="40%"><a id="Warning"></a><a id="warning"></a><a id="WARNING"></a><dl>
<dt><b>Warning</b></dt>
</dl>
</td>
<td width="60%">
Indicates a problem that is not immediately significant, but may cause future problems.

</td>
</tr>
</table>

### -param wszProvName [in]

The provider name.

### -param wszMessage [in]

The event description.

## -returns

If the function succeeds, the return value is S_OK. Otherwise, the return value is one of the error codes defined in WinError.h.

## -remarks

This function provides the time provider with a simplified interface for event logging. Time providers that require more extensive event logging can perform their own event logging. For more information on event logging, see 
<a href="/windows/desktop/EventLog/event-logging">Event Logging</a>.

The 
<a href="/windows/desktop/api/timeprov/nf-timeprov-timeprovopen">TimeProvOpen</a> function returns a pointer to this function.

## -see-also

<a href="/windows/desktop/api/timeprov/nf-timeprov-timeprovopen">TimeProvOpen</a>
