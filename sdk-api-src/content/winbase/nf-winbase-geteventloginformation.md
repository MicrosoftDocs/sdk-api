---
UID: NF:winbase.GetEventLogInformation
title: GetEventLogInformation function (winbase.h)
description: Retrieves information about the specified event log.
helpviewer_keywords: ["EVENTLOG_FULL_INFO","GetEventLogInformation","GetEventLogInformation function","_win32_geteventloginformation","base.geteventloginformation","winbase/GetEventLogInformation"]
old-location: base\geteventloginformation.htm
tech.root: base
ms.assetid: 627e0af2-3ce6-47fe-89c6-d7c0483cb94b
ms.date: 12/05/2018
ms.keywords: EVENTLOG_FULL_INFO, GetEventLogInformation, GetEventLogInformation function, _win32_geteventloginformation, base.geteventloginformation, winbase/GetEventLogInformation
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetEventLogInformation
 - winbase/GetEventLogInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-EventLog-Legacy-l1-1-0.dll
 - advapi32legacy.dll
api_name:
 - GetEventLogInformation
---

# GetEventLogInformation function


## -description

Retrieves information about the specified event log.

## -parameters

### -param hEventLog [in]

A handle to the event log. The 
<a href="/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-registereventsourcea">RegisterEventSource</a> function returns this handle.

### -param dwInfoLevel [in]

The level of event log information to return. 

This parameter can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENTLOG_FULL_INFO"></a><a id="eventlog_full_info"></a><dl>
<dt><b>EVENTLOG_FULL_INFO</b></dt>
</dl>
</td>
<td width="60%">
Indicate whether the specified log is full. The <i>lpBuffer</i> parameter will contain an 
<a href="/windows/desktop/api/winbase/ns-winbase-eventlog_full_information">EVENTLOG_FULL_INFORMATION</a> structure.

</td>
</tr>
</table>

### -param lpBuffer [out]

An application-allocated buffer that receives the event log information. The format of this data depends on the value of the <i>dwInfoLevel</i> parameter.

### -param cbBufSize [in]

The size of the <i>lpBuffer</i> buffer, in bytes.

### -param pcbBytesNeeded [out]

The function sets this parameter to the required buffer size for the requested information, regardless of whether the function succeeds. Use this value if the function fails with <b>ERROR_INSUFFICIENT_BUFFER</b> to allocate a buffer of the correct size.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/winbase/ns-winbase-eventlog_full_information">EVENTLOG_FULL_INFORMATION</a>



<a href="/windows/desktop/EventLog/event-logging-functions">Event Logging Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a>



<a href="/windows/desktop/api/winbase/nf-winbase-registereventsourcea">RegisterEventSource</a>