---
UID: NF:evntcons.EventAccessControl
title: EventAccessControl function (evntcons.h)
description: Adds or modifies the permissions of the specified provider or session.
helpviewer_keywords: ["EventAccessControl","EventAccessControl function [ETW]","TRACELOG_ACCESS_KERNEL_LOGGER","TRACELOG_ACCESS_REALTIME","TRACELOG_CREATE_ONDISK","TRACELOG_CREATE_REALTIME","TRACELOG_GUID_ENABLE","TRACELOG_LOG_EVENT","TRACELOG_REGISTER_GUIDS","WMIGUID_QUERY","base.eventaccesscontrol_func","etw.eventaccesscontrol_func","evntcons/EventAccessControl"]
old-location: etw\eventaccesscontrol_func.htm
tech.root: ETW
ms.assetid: 699bb165-680f-4d3b-8859-959f319ca4be
ms.date: 12/05/2018
ms.keywords: EventAccessControl, EventAccessControl function [ETW], TRACELOG_ACCESS_KERNEL_LOGGER, TRACELOG_ACCESS_REALTIME, TRACELOG_CREATE_ONDISK, TRACELOG_CREATE_REALTIME, TRACELOG_GUID_ENABLE, TRACELOG_LOG_EVENT, TRACELOG_REGISTER_GUIDS, WMIGUID_QUERY, base.eventaccesscontrol_func, etw.eventaccesscontrol_func, evntcons/EventAccessControl
req.header: evntcons.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Sechost.lib on Windows 8.1 and Windows Server 2012; Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008 and Windows Vista
req.dll: Sechost.dll on Windows 8.1 and Windows Server 2012; Advapi32.dll on Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows Server 2008 and Windows Vista
req.irql: 
req.typenames: 
targetos: Windows
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EventAccessControl
 - evntcons/EventAccessControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-eventing-controller-l1-1-1.dll
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Sechost.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvAPI32-l2-1-1.dll
 - API-MS-Win-Eventing-Controller-l1-1-0.dll
 - KernelBase.dll
api_name:
 - EventAccessControl
---

# EventAccessControl function (evntcons.h)


## -description

Adds or modifies the permissions of the specified provider or session.

## -parameters

### -param Guid [in]

GUID that uniquely identifies the provider or session whose permissions you want to add or modify.

### -param Operation [in]

Type of operation to perform, for example, add a DACL to the session's GUID or provider's GUID. For 
      possible values, see the <a href="/windows/desktop/api/evntcons/ne-evntcons-eventsecurityoperation">EVENTSECURITYOPERATION</a> 
      enumeration.

### -param Sid [in]

The security identifier (SID) of the user  or group to whom you want to grant or deny permissions.

### -param Rights [in]

You can specify one or more of the following permissions:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WMIGUID_QUERY"></a><a id="wmiguid_query"></a><dl>
<dt><b>WMIGUID_QUERY</b></dt>
</dl>
</td>
<td width="60%">
Allows the user to query information about the trace session. Set this permission on the session's 
        GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="TRACELOG_CREATE_REALTIME"></a><a id="tracelog_create_realtime"></a><dl>
<dt><b>TRACELOG_CREATE_REALTIME</b></dt>
</dl>
</td>
<td width="60%">
Allows the user to start or update a real-time session. Set this permission on the session's GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="TRACELOG_CREATE_ONDISK"></a><a id="tracelog_create_ondisk"></a><dl>
<dt><b>TRACELOG_CREATE_ONDISK</b></dt>
</dl>
</td>
<td width="60%">
Allows the user to start or update a session that writes events  to a log file. Set this permission on 
        the session's GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="TRACELOG_GUID_ENABLE"></a><a id="tracelog_guid_enable"></a><dl>
<dt><b>TRACELOG_GUID_ENABLE</b></dt>
</dl>
</td>
<td width="60%">
Allows the user to enable the provider. Set this permission on the provider's GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="TRACELOG_ACCESS_KERNEL_LOGGER"></a><a id="tracelog_access_kernel_logger"></a><dl>
<dt><b>TRACELOG_ACCESS_KERNEL_LOGGER</b></dt>
</dl>
</td>
<td width="60%">
Not used.

</td>
</tr>
<tr>
<td width="40%"><a id="TRACELOG_LOG_EVENT"></a><a id="tracelog_log_event"></a><dl>
<dt><b>TRACELOG_LOG_EVENT</b></dt>
</dl>
</td>
<td width="60%">
Allows the user to log events to a trace session if session is running in  SECURE mode (the session set 
        the EVENT_TRACE_SECURE_MODE flag in the LogFileMode member of EVENT_TRACE_PROPERTIES).

</td>
</tr>
<tr>
<td width="40%"><a id="TRACELOG_ACCESS_REALTIME"></a><a id="tracelog_access_realtime"></a><dl>
<dt><b>TRACELOG_ACCESS_REALTIME</b></dt>
</dl>
</td>
<td width="60%">
Allows a user to consume events in real-time. Set this permission on the session's GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="TRACELOG_REGISTER_GUIDS"></a><a id="tracelog_register_guids"></a><dl>
<dt><b>TRACELOG_REGISTER_GUIDS</b></dt>
</dl>
</td>
<td width="60%">
Allows the user to register the provider.  Set this permission on the provider's GUID.

</td>
</tr>
</table>

### -param AllowOrDeny [in]

If <b>TRUE</b>, grant the user permissions to the session or provider; otherwise, deny 
      permissions. This value is ignored if the value of <i>Operation</i> is EventSecuritySetSACL 
      or EventSecurityAddSACL.

## -returns

Returns ERROR_SUCCESS if successful.

## -remarks

By default, only the administrator of the computer, users in the Performance Log Users group, and services 
     running as LocalSystem, LocalService, NetworkService can control trace sessions and provide and consume event 
     data. Only users with administrative privileges and services running as LocalSystem can start and control an 
     NT Kernel Logger session.

<b>Windows Server 2003:  </b>Only users with administrator privileges can control trace sessions and consume event data; any user can provide event data.

<b>Windows XP and Windows 2000:  </b>Any user can control trace sessions and provide and consume event data.

Users with administrator privileges can control trace sessions if the tool that they use to control the session 
     is started from a Command Prompt window that is opened with 
     <b>Run as administrator...</b>.

To grant a restricted user the ability to control trace sessions, you can add them to the Performance Log Users 
    group or call this function to grant them permission. For example, you can grant user A permission to start and 
    stop a trace session and grant user B permission to only query the session.

To restrict who can log events to the session, see the TRACELOG_LOG_EVENT permission.

The ACL on the log file determines who can consume event data from the log file. To consume events from a 
    session in real-time, you must grant the user TRACELOG_ACCESS_REALTIME permission or the user must be a member of 
    the Performance Log Users group.

You can also specify the provider's GUID to restrict who can register the provider and who can enable the 
    provider.

## -see-also

<a href="/windows/desktop/api/evntcons/nf-evntcons-eventaccessquery">EventAccessQuery</a>



<a href="/windows/desktop/api/evntcons/nf-evntcons-eventaccessremove">EventAccessRemove</a>