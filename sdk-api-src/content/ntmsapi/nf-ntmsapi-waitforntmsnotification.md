---
UID: NF:ntmsapi.WaitForNtmsNotification
title: WaitForNtmsNotification function (ntmsapi.h)
description: The WaitForNtmsNotification function waits for the next object change notification.
helpviewer_keywords: ["WaitForNtmsNotification","WaitForNtmsNotification function [Files]","_zaw_waitforntmsnotification","base.waitforntmsnotification","fs.waitforntmsnotification","ntmsapi/WaitForNtmsNotification"]
old-location: fs\waitforntmsnotification.htm
tech.root: fs
ms.assetid: ecb39bac-f062-4835-bbae-f9f643ffde9b
ms.date: 12/05/2018
ms.keywords: WaitForNtmsNotification, WaitForNtmsNotification function [Files], _zaw_waitforntmsnotification, base.waitforntmsnotification, fs.waitforntmsnotification, ntmsapi/WaitForNtmsNotification
req.header: ntmsapi.h
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
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WaitForNtmsNotification
 - ntmsapi/WaitForNtmsNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - WaitForNtmsNotification
---

# WaitForNtmsNotification function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>WaitForNtmsNotification</b> function waits for the next object change notification.

## -parameters

### -param hNotification [in]

Notification handle returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmsnotification">OpenNtmsNotification</a> function.

### -param lpNotificationInformation [out]

Pointer to an 
<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_notificationinformation">NTMS_NOTIFICATIONINFORMATION</a> structure that receives the notification information.

### -param dwTimeout [in]

Maximum number of milliseconds to wait. If you specify a value of INFINITE, this function will not time-out.

## -returns

This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The database query or update failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>hNotification</i> parameter is <b>NULL</b> or is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_DATA</b></dt>
</dl>
</td>
<td width="60%">
Notification pipe failed. Attempt to set up notification again.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Unable to connect to the RSM service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The time-out event expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successfully executed.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-closentmsnotification">CloseNtmsNotification</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Database Notification Functions</a>



<a href="/windows/desktop/api/ntmsapi/ns-ntmsapi-ntms_notificationinformation">NTMS_NOTIFICATIONINFORMATION</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmsnotification">OpenNtmsNotification</a>