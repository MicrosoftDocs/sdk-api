---
UID: NF:winbase.ReportEventW
title: ReportEventW function (winbase.h)
description: Writes an entry at the end of the specified event log. (Unicode)
helpviewer_keywords: ["EVENTLOG_AUDIT_FAILURE", "EVENTLOG_AUDIT_SUCCESS", "EVENTLOG_ERROR_TYPE", "EVENTLOG_INFORMATION_TYPE", "EVENTLOG_SUCCESS", "EVENTLOG_WARNING_TYPE", "ReportEvent", "ReportEvent function", "ReportEventW", "_win32_reportevent", "base.reportevent", "winbase/ReportEvent", "winbase/ReportEventW"]
old-location: base\reportevent.htm
tech.root: base
ms.assetid: e39273c3-9e42-41a1-9ec1-1cdff2ab7b55
ms.date: 12/05/2018
ms.keywords: EVENTLOG_AUDIT_FAILURE, EVENTLOG_AUDIT_SUCCESS, EVENTLOG_ERROR_TYPE, EVENTLOG_INFORMATION_TYPE, EVENTLOG_SUCCESS, EVENTLOG_WARNING_TYPE, ReportEvent, ReportEvent function, ReportEventA, ReportEventW, _win32_reportevent, base.reportevent, winbase/ReportEvent, winbase/ReportEventA, winbase/ReportEventW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ReportEventW (Unicode) and ReportEventA (ANSI)
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
 - ReportEventW
 - winbase/ReportEventW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-advapi32-eventlog-l1-1-2.dll
 - Advapi32.dll
 - API-MS-Win-EventLog-Legacy-l1-1-0.dll
 - advapi32legacy.dll
 - Ext-MS-Win-AdvAPI32-EventLog-l1-1-0.dll
 - Ext-Ms-Win-AdvAPI32-EventLog-L1-1-1.dll
api_name:
 - ReportEvent
 - ReportEventA
 - ReportEventW
---

# ReportEventW function


## -description

Writes an entry at the end of the specified event log.

## -parameters

### -param hEventLog [in]

A handle to the event log. The 
<a href="/windows/desktop/api/winbase/nf-winbase-registereventsourcea">RegisterEventSource</a> function returns this handle. 

As of Windows XP with SP2, this parameter cannot be a handle to the <b>Security</b> log. To write an event to the <b>Security</b> log, use the <a href="/windows/desktop/api/authz/nf-authz-authzreportsecurityevent">AuthzReportSecurityEvent</a> function.

### -param wType [in]

The type of event to be logged. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENTLOG_SUCCESS"></a><a id="eventlog_success"></a><dl>
<dt><b>EVENTLOG_SUCCESS</b></dt>
<dt>0x0000</dt>
</dl>
</td>
<td width="60%">
Information event

</td>
</tr>
<tr>
<td width="40%"><a id="EVENTLOG_AUDIT_FAILURE"></a><a id="eventlog_audit_failure"></a><dl>
<dt><b>EVENTLOG_AUDIT_FAILURE</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Failure Audit event

</td>
</tr>
<tr>
<td width="40%"><a id="EVENTLOG_AUDIT_SUCCESS"></a><a id="eventlog_audit_success"></a><dl>
<dt><b>EVENTLOG_AUDIT_SUCCESS</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Success Audit event

</td>
</tr>
<tr>
<td width="40%"><a id="EVENTLOG_ERROR_TYPE"></a><a id="eventlog_error_type"></a><dl>
<dt><b>EVENTLOG_ERROR_TYPE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Error event

</td>
</tr>
<tr>
<td width="40%"><a id="EVENTLOG_INFORMATION_TYPE"></a><a id="eventlog_information_type"></a><dl>
<dt><b>EVENTLOG_INFORMATION_TYPE</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Information event

</td>
</tr>
<tr>
<td width="40%"><a id="EVENTLOG_WARNING_TYPE"></a><a id="eventlog_warning_type"></a><dl>
<dt><b>EVENTLOG_WARNING_TYPE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Warning event

</td>
</tr>
</table>
 

For more information about event types, see 
<a href="/windows/desktop/EventLog/event-types">Event Types</a>.

### -param wCategory [in]

The event category. This is source-specific information; the category can have any value. For more information, see 
<a href="/windows/desktop/EventLog/event-categories">Event Categories</a>.

### -param dwEventID [in]

The event identifier. The event identifier specifies the entry in the message file associated with the event source. For more information, see <a href="/windows/desktop/EventLog/event-identifiers">Event Identifiers</a>.

### -param lpUserSid [in]

A pointer to the current user's security identifier. This parameter can be <b>NULL</b> if the security identifier is not required.

### -param wNumStrings [in]

The number of insert strings in the array pointed to by the <i>lpStrings</i> parameter. A value of zero indicates that no strings are present.

### -param dwDataSize [in]

The number of bytes of event-specific raw (binary) data to write to the log. If this parameter is zero, no event-specific data is present.

### -param lpStrings [in]

A pointer to a buffer containing an array of null-terminated strings that are merged into the message before Event Viewer displays the string to the user. This parameter must be a valid pointer (or <b>NULL</b>), even if <i>wNumStrings</i> is zero. Each string is limited to 31,839  characters.

<b>Prior to Windows Vista:  </b>Each string is limited to 32K characters.

### -param lpRawData [in]

A pointer to the buffer containing the binary data. This parameter must be a valid pointer (or <b>NULL</b>), even if the <i>dwDataSize</i> parameter is zero.

## -returns

If the function succeeds, the return value is nonzero, indicating that the entry was written to the log.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>, which returns one of the following extended error codes.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not valid.

This error is returned on Windows Server 2003 if the  message data to be logged is too large. This error is returned by the RPC server on Windows Server 2003 if the <i>dwDataSize</i> parameter is larger than 261,991 (0x3ff67).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory resources are available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BOUND</b></dt>
</dl>
</td>
<td width="60%">
The array bounds are invalid. 

This error is returned if the  message data to be logged is too large. On Windows Vista and later, this error is returned if the <i>dwDataSize</i> parameter is larger than 61,440 (0xf000).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_X_BAD_STUB_DATA</b></dt>
</dl>
</td>
<td width="60%">
The stub received bad data.

This error is returned on Windows XP if the  message data to be logged is too large. This error is returned by the RPC server on Windows XP, if the <i>dwDataSize</i> parameter is larger than 262,143 (0x3ffff).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

This function is used to log an event. The entry is written to the end of the configured log for the source identified by the <i>hEventLog</i> parameter. The 
<b>ReportEvent</b> function adds the time, the entry's length, and the offsets before storing the entry in the log. To enable the function to add the user name, you must supply the user's SID in the <i>lpUserSid</i> parameter.

There are different size limits on the size of the message data that can be logged depending on the version of Windows used by both the client where the application is run and the server where the message is logged. The server is determined by the <i>lpUNCServerName</i> parameter passed to the <a href="/windows/desktop/api/winbase/nf-winbase-registereventsourcea">RegisterEventSource</a> function. Different errors are returned when the size limit is exceeded that depend on the version of Windows.

If the string that you log contains %<i>n</i>, where <i>n</i> is an integer value (for example, %1), the event viewer treats it as an insertion string. Because an IPv6 address can contain this character sequence, you must provide a format specifier (<i>!S!</i>) to log an event message that contains an IPv6 address. This specifier tells the formatting code to use the string literally and not perform any further expansions (for example, "my IPv6 address is: %1!S!").


#### Examples

For an example, see 
<a href="/windows/desktop/EventLog/reporting-an-event">Reporting an Event</a>.

<div class="code"></div>




> [!NOTE]
> The winbase.h header defines ReportEvent as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-cleareventloga">ClearEventLog</a>



<a href="/windows/desktop/api/winbase/nf-winbase-closeeventlog">CloseEventLog</a>



<a href="/windows/desktop/EventLog/event-log-file-format">Event Log File Format</a>



<a href="/windows/desktop/EventLog/event-logging-functions">Event Logging Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openeventloga">OpenEventLog</a>



<a href="/windows/desktop/api/winbase/nf-winbase-readeventloga">ReadEventLog</a>



<a href="/windows/desktop/api/winbase/nf-winbase-registereventsourcea">RegisterEventSource</a>
