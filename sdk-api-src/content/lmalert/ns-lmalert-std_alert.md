---
UID: NS:lmalert._STD_ALERT
title: STD_ALERT (lmalert.h)
description: The STD_ALERT structure contains the time and date when a significant event occurred.
helpviewer_keywords: ["*LPSTD_ALERT","*PSTD_ALERT","ALERT_ADMIN_EVENT","ALERT_ERRORLOG_EVENT","ALERT_MESSAGE_EVENT","ALERT_PRINT_EVENT","ALERT_USER_EVENT","LPSTD_ALERT","LPSTD_ALERT structure pointer [Network Management]","PSTD_ALERT","PSTD_ALERT structure pointer [Network Management]","STD_ALERT","STD_ALERT structure [Network Management]","_win32_std_alert_str","lmalert/LPSTD_ALERT","lmalert/PSTD_ALERT","lmalert/STD_ALERT","netmgmt.std_alert_str"]
old-location: netmgmt\std_alert_str.htm
tech.root: NetMgmt
ms.assetid: daa4594f-e59e-4f05-8183-677bee4ea446
ms.date: 12/05/2018
ms.keywords: '*LPSTD_ALERT, *PSTD_ALERT, ALERT_ADMIN_EVENT, ALERT_ERRORLOG_EVENT, ALERT_MESSAGE_EVENT, ALERT_PRINT_EVENT, ALERT_USER_EVENT, LPSTD_ALERT, LPSTD_ALERT structure pointer [Network Management], PSTD_ALERT, PSTD_ALERT structure pointer [Network Management], STD_ALERT, STD_ALERT structure [Network Management], _win32_std_alert_str, lmalert/LPSTD_ALERT, lmalert/PSTD_ALERT, lmalert/STD_ALERT, netmgmt.std_alert_str'
req.header: lmalert.h
req.include-header: Lm.h
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
req.typenames: STD_ALERT, *PSTD_ALERT, *LPSTD_ALERT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _STD_ALERT
 - lmalert/_STD_ALERT
 - PSTD_ALERT
 - lmalert/PSTD_ALERT
 - STD_ALERT
 - lmalert/STD_ALERT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmalert.h
api_name:
 - STD_ALERT
---

# STD_ALERT structure


## -description

The
				<b>STD_ALERT</b> structure contains the time and date when a significant event occurred. The structure also contains an alert class and the name of the application that is raising the alert message. You must specify the 
<b>STD_ALERT</b> structure when you send an alert message using the 
<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraise">NetAlertRaise</a> function.

## -struct-fields

### -field alrt_timestamp

Type: <b>DWORD</b>

The time and date of the event. This value is stored as the number of seconds that have elapsed since 00:00:00, January 1, 1970, GMT.

### -field alrt_eventname

Type: <b>WCHAR[EVLEN + 1]</b>

A Unicode string indicating the alert class (type of event). This parameter can be one of the following predefined values, or another alert class that you have defined for network applications. (The event name for an alert can be any text string.) 



<table>
<tr>
<th>Name</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ALERT_ADMIN_EVENT"></a><a id="alert_admin_event"></a><dl>
<dt><b>ALERT_ADMIN_EVENT</b></dt>
</dl>
</td>
<td width="60%">
An administrator's intervention is required.

</td>
</tr>
<tr>
<td width="40%"><a id="ALERT_ERRORLOG_EVENT"></a><a id="alert_errorlog_event"></a><dl>
<dt><b>ALERT_ERRORLOG_EVENT</b></dt>
</dl>
</td>
<td width="60%">
An entry was added to the error log.

</td>
</tr>
<tr>
<td width="40%"><a id="ALERT_MESSAGE_EVENT"></a><a id="alert_message_event"></a><dl>
<dt><b>ALERT_MESSAGE_EVENT</b></dt>
</dl>
</td>
<td width="60%">
A user or application received a broadcast message.

</td>
</tr>
<tr>
<td width="40%"><a id="ALERT_PRINT_EVENT"></a><a id="alert_print_event"></a><dl>
<dt><b>ALERT_PRINT_EVENT</b></dt>
</dl>
</td>
<td width="60%">
A print job completed or a print error occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="ALERT_USER_EVENT"></a><a id="alert_user_event"></a><dl>
<dt><b>ALERT_USER_EVENT</b></dt>
</dl>
</td>
<td width="60%">
An application or resource was used.

</td>
</tr>
</table>

### -field alrt_servicename

Type: <b>WCHAR[SNLEN + 1]</b>

A Unicode string indicating the service application that is raising the alert message.

## -remarks

The 
<b>STD_ALERT</b> structure must be followed by one 
<a href="/windows/desktop/api/lmalert/ns-lmalert-admin_other_info">ADMIN_OTHER_INFO</a>, 
<a href="/windows/desktop/api/lmalert/ns-lmalert-errlog_other_info">ERRLOG_OTHER_INFO</a>, 
<a href="/windows/desktop/api/lmalert/ns-lmalert-print_other_info">PRINT_OTHER_INFO</a>, or 
<a href="/windows/desktop/api/lmalert/ns-lmalert-user_other_info">USER_OTHER_INFO</a> structure. These structures can optionally be followed by variable-length data. The calling application must allocate the memory for all structures and variable-length data in an alert message buffer.

See 
<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraise">NetAlertRaise</a> for a code sample that raises an administrative alert using a 
<b>STD_ALERT</b> structure and an 
<a href="/windows/desktop/api/lmalert/ns-lmalert-admin_other_info">ADMIN_OTHER_INFO</a> structure.

## -see-also

<a href="/windows/desktop/api/lmalert/ns-lmalert-admin_other_info">ADMIN_OTHER_INFO</a>



<a href="/windows/desktop/NetMgmt/alert-functions">Alert Functions</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-errlog_other_info">ERRLOG_OTHER_INFO</a>



<a href="/windows/desktop/api/lmalert/nf-lmalert-netalertraise">NetAlertRaise</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-print_other_info">PRINT_OTHER_INFO</a>



<a href="/windows/desktop/api/lmalert/ns-lmalert-user_other_info">USER_OTHER_INFO</a>