---
UID: NS:winnt._EVENTLOGRECORD
title: EVENTLOGRECORD (winnt.h)
description: Contains information about an event record returned by the ReadEventLog function.
helpviewer_keywords: ["*PEVENTLOGRECORD","EVENTLOGRECORD","EVENTLOGRECORD structure","EVENTLOG_AUDIT_FAILURE","EVENTLOG_AUDIT_SUCCESS","EVENTLOG_ERROR_TYPE","EVENTLOG_INFORMATION_TYPE","EVENTLOG_WARNING_TYPE","PEVENTLOGRECORD","PEVENTLOGRECORD structure pointer","_EVENTLOGRECORD","_win32_eventlogrecord_str","base.eventlogrecord_str","winnt/EVENTLOGRECORD","winnt/PEVENTLOGRECORD"]
old-location: base\eventlogrecord_str.htm
tech.root: base
ms.assetid: 669b182a-bc81-4386-9815-6ffa09e2e743
ms.date: 12/05/2018
ms.keywords: '*PEVENTLOGRECORD, EVENTLOGRECORD, EVENTLOGRECORD structure, EVENTLOG_AUDIT_FAILURE, EVENTLOG_AUDIT_SUCCESS, EVENTLOG_ERROR_TYPE, EVENTLOG_INFORMATION_TYPE, EVENTLOG_WARNING_TYPE, PEVENTLOGRECORD, PEVENTLOGRECORD structure pointer, _EVENTLOGRECORD, _win32_eventlogrecord_str, base.eventlogrecord_str, winnt/EVENTLOGRECORD, winnt/PEVENTLOGRECORD'
req.header: winnt.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: EVENTLOGRECORD, *PEVENTLOGRECORD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVENTLOGRECORD
 - winnt/_EVENTLOGRECORD
 - PEVENTLOGRECORD
 - winnt/PEVENTLOGRECORD
 - EVENTLOGRECORD
 - winnt/EVENTLOGRECORD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - EVENTLOGRECORD
---

# EVENTLOGRECORD structure


## -description

Contains information about an event record returned by the 
<a href="/windows/desktop/api/winbase/nf-winbase-readeventloga">ReadEventLog</a> function.

## -struct-fields

### -field Length

The size of this event record, in bytes. Note that this value is stored at both ends of the entry to ease moving forward or backward through the log. The length includes any pad bytes inserted at the end of the record for <b>DWORD</b> alignment.

### -field Reserved

A DWORD value that is always set to <b>ELF_LOG_SIGNATURE</b> (the value is 0x654c664c), which is ASCII for eLfL.

### -field RecordNumber

The number of the record. This value can be used with the EVENTLOG_SEEK_READ flag in the 
<a href="/windows/desktop/api/winbase/nf-winbase-readeventloga">ReadEventLog</a> function to begin reading at a specified record. For more information, see 
<a href="/windows/desktop/EventLog/event-log-records">Event Log Records</a>.

### -field TimeGenerated

The time at which this entry was submitted. This time is measured in the number of seconds elapsed since 00:00:00 January 1, 1970, Universal Coordinated Time.

### -field TimeWritten

The time at which this entry was received by the service to be written to the log. This time is measured in the number of seconds elapsed since 00:00:00 January 1, 1970, Universal Coordinated Time.

### -field EventID

The event identifier. The value is specific to the event source for the event, and is used with source name to locate a description string in the message file for the event source. For more information, see 
<a href="/windows/desktop/EventLog/event-identifiers">Event Identifiers</a>.

### -field EventType

The type of event. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
 

For more information, see 
<a href="/windows/desktop/EventLog/event-types">Event Types</a>.

### -field NumStrings

The number of strings present in the log (at the position indicated by <b>StringOffset</b>). These strings are merged into the message before it is displayed to the user.

### -field EventCategory

The category for this event. The meaning of this value depends on the event source. For more information, see 
<a href="/windows/desktop/EventLog/event-categories">Event Categories</a>.

### -field ReservedFlags

Reserved.

### -field ClosingRecordNumber

Reserved.

### -field StringOffset

The offset of the description strings within this event log record.

### -field UserSidLength

The size of the <b>UserSid</b> member, in bytes. This value can be zero if no security identifier was provided.

### -field UserSidOffset

The offset of the security identifier (SID) within this event log record. To obtain the user name for this SID, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountsida">LookupAccountSid</a> function.

### -field DataLength

The size of the event-specific data (at the position indicated by <b>DataOffset</b>), in bytes.

### -field DataOffset

The offset of the event-specific information within this event log record, in bytes. This information could be something specific (a disk driver might log the number of retries, for example), followed by binary information specific to the event being logged and to the source that generated the entry.

## -remarks

The defined members are followed by the replacement strings for the message identified by the event identifier, the binary information, some pad bytes to make sure the full entry is on a <b>DWORD</b> boundary, and finally the length of the log entry again. Because the strings and the binary information can be of any length, no structure members are defined to reference them. The declaration of this structure in Winnt.h describes these members as follows:


``` syntax
    // WCHAR SourceName[]
    // WCHAR Computername[]
    // SID   UserSid
    // WCHAR Strings[]
    // BYTE  Data[]
    // CHAR  Pad[]
    // DWORD Length;
```

The source name is a variable-length string that specifies the name of the event source. The computer name is the name of the computer that generated the event. It may be followed with some padding bytes so that the user SID is aligned on a <b>DWORD</b> boundary. The user SID identifies the active user at the time this event was logged. If <b>UserSidLength</b> is zero, this field may be empty.

The event identifier together with source name and a language identifier identify a string that describes the event in more detail. The strings are used as replacement strings and are merged into the message string to make a complete message. The message strings are contained in a message file specified in the source entry in the registry. To obtain the appropriate message string from the message file, load the message file with the 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> function and use the 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function.

The binary information is information that is specific to the event. It could be the contents of the processor registers when a device driver got an error, a dump of an invalid packet that was received from the network, a dump of all the structures in a program (when the data area was detected to be corrupt), and so on. This information should be useful to the writer of the device driver or the application in tracking down bugs or unauthorized breaks into the application.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountsida">LookupAccountSid</a>



<a href="/windows/desktop/api/winbase/nf-winbase-readeventloga">ReadEventLog</a>
