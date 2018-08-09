---
UID: NS:lmalert._STD_ALERT
title: "_STD_ALERT"
author: windows-sdk-content
description: The STD_ALERT structure contains the time and date when a significant event occurred.
old-location: netmgmt\std_alert_str.htm
old-project: netmgmt
ms.assetid: daa4594f-e59e-4f05-8183-677bee4ea446
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*LPSTD_ALERT, *PSTD_ALERT, ALERT_ADMIN_EVENT, ALERT_ERRORLOG_EVENT, ALERT_MESSAGE_EVENT, ALERT_PRINT_EVENT, ALERT_USER_EVENT, LPSTD_ALERT, LPSTD_ALERT structure pointer [Network Management], PSTD_ALERT, PSTD_ALERT structure pointer [Network Management], STD_ALERT, STD_ALERT structure [Network Management], _STD_ALERT, _win32_std_alert_str, lmalert/LPSTD_ALERT, lmalert/PSTD_ALERT, lmalert/STD_ALERT, netmgmt.std_alert_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: STD_ALERT, *PSTD_ALERT, *LPSTD_ALERT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmalert.h
api_name:
 - STD_ALERT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _STD_ALERT structure


## -description


The
				<b>STD_ALERT</b> structure contains the time and date when a significant event occurred. The structure also contains an alert class and the name of the application that is raising the alert message. You must specify the 
<b>STD_ALERT</b> structure when you send an alert message using the 
<a href="https://msdn.microsoft.com/11367a72-c21d-4044-98cf-a7a30cc43a8b">NetAlertRaise</a> function.


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
<a href="https://msdn.microsoft.com/43119dcf-7d04-4e3b-b1dc-20e814fbdc2f">ADMIN_OTHER_INFO</a>, 
<a href="https://msdn.microsoft.com/832ebe88-e1c4-4ce3-8057-922419b577f7">ERRLOG_OTHER_INFO</a>, 
<a href="https://msdn.microsoft.com/f2fd87bc-abde-43c0-b29d-d43cc5f038b8">PRINT_OTHER_INFO</a>, or 
<a href="https://msdn.microsoft.com/2f6bd906-fdab-410a-8856-4482e047371f">USER_OTHER_INFO</a> structure. These structures can optionally be followed by variable-length data. The calling application must allocate the memory for all structures and variable-length data in an alert message buffer.

See 
<a href="https://msdn.microsoft.com/11367a72-c21d-4044-98cf-a7a30cc43a8b">NetAlertRaise</a> for a code sample that raises an administrative alert using a 
<b>STD_ALERT</b> structure and an 
<a href="https://msdn.microsoft.com/43119dcf-7d04-4e3b-b1dc-20e814fbdc2f">ADMIN_OTHER_INFO</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/43119dcf-7d04-4e3b-b1dc-20e814fbdc2f">ADMIN_OTHER_INFO</a>



<a href="https://msdn.microsoft.com/e131191b-7413-45ff-84cd-b3a873d33ca1">Alert Functions</a>



<a href="https://msdn.microsoft.com/832ebe88-e1c4-4ce3-8057-922419b577f7">ERRLOG_OTHER_INFO</a>



<a href="https://msdn.microsoft.com/11367a72-c21d-4044-98cf-a7a30cc43a8b">NetAlertRaise</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/f2fd87bc-abde-43c0-b29d-d43cc5f038b8">PRINT_OTHER_INFO</a>



<a href="https://msdn.microsoft.com/2f6bd906-fdab-410a-8856-4482e047371f">USER_OTHER_INFO</a>
 

 

