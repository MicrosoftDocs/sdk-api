---
UID: NF:ntmsapi.OpenNtmsNotification
title: OpenNtmsNotification function (ntmsapi.h)
description: The OpenNtmsNotification function opens a channel to receive RSM object change notifications for objects of the specified type.
helpviewer_keywords: ["OpenNtmsNotification","OpenNtmsNotification function [Files]","_zaw_openntmsnotification","base.openntmsnotification","fs.openntmsnotification","ntmsapi/OpenNtmsNotification"]
old-location: fs\openntmsnotification.htm
tech.root: fs
ms.assetid: a5b6ab4a-ab4c-4c84-877f-824dc9ac19a7
ms.date: 12/05/2018
ms.keywords: OpenNtmsNotification, OpenNtmsNotification function [Files], _zaw_openntmsnotification, base.openntmsnotification, fs.openntmsnotification, ntmsapi/OpenNtmsNotification
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
 - OpenNtmsNotification
 - ntmsapi/OpenNtmsNotification
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
 - OpenNtmsNotification
---

# OpenNtmsNotification function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>OpenNtmsNotification</b> function opens a channel to receive RSM object change notifications for objects of the specified type.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

### -param dwType [in]

RSM object type for notification. For a list of values, see 
<a href="/windows/desktop/api/ntmsapi/ne-ntmsapi-ntmsobjectstypes">NtmsObjectsTypes</a>.

## -returns

The 
<b>OpenNtmsNotification</b> function returns a notification handle that you pass to the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-waitforntmsnotification">WaitForNtmsNotification</a> or 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-closentmsnotification">CloseNtmsNotification</a> functions.

For extended error information, call the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. This function can return one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
 NTMS_USE_ACCESS to the computer is denied. Other security errors are also possible, but they would indicate a security subsystem error.

<b>Windows XP:  </b>No access rights are required.

</td>
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
The value specified in the <i>hSession</i> parameter is <b>NULL</b> or is not valid.

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
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INVALID_HANDLE_VALUE</b></dt>
</dl>
</td>
<td width="60%">
The function failed.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-closentmsnotification">CloseNtmsNotification</a>



<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Database Notification Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-waitforntmsnotification">WaitForNtmsNotification</a>