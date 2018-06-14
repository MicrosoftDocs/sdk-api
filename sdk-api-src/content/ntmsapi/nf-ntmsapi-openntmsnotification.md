---
UID: NF:ntmsapi.OpenNtmsNotification
title: OpenNtmsNotification function
author: windows-sdk-content
description: The OpenNtmsNotification function opens a channel to receive RSM object change notifications for objects of the specified type.
old-location: fs\openntmsnotification.htm
old-project: Rsm
ms.assetid: a5b6ab4a-ab4c-4c84-877f-824dc9ac19a7
ms.author: windowssdkdev
ms.date: 04/05/2018
ms.keywords: OpenNtmsNotification, OpenNtmsNotification function [Files], _zaw_openntmsnotification, base.openntmsnotification, fs.openntmsnotification, ntmsapi/OpenNtmsNotification
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - OpenNtmsNotification
product: Windows
targetos: Windows
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# OpenNtmsNotification function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>OpenNtmsNotification</b> function opens a channel to receive RSM object change notifications for objects of the specified type.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param dwType [in]

RSM object type for notification. For a list of values, see 
<a href="https://msdn.microsoft.com/598e7cb1-f463-4252-9bdf-ccb98f36f4da">NtmsObjectsTypes</a>.


## -returns



The 
<b>OpenNtmsNotification</b> function returns a notification handle that you pass to the 
<a href="https://msdn.microsoft.com/ecb39bac-f062-4835-bbae-f9f643ffde9b">WaitForNtmsNotification</a> or 
<a href="https://msdn.microsoft.com/30aa06af-70d4-45c0-b624-575dcf867efb">CloseNtmsNotification</a> functions.

For extended error information, call the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. This function can return one of the following values.

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




<a href="https://msdn.microsoft.com/30aa06af-70d4-45c0-b624-575dcf867efb">CloseNtmsNotification</a>



<a href="removable_storage_manager_functions.htm">Database Notification Functions</a>



<a href="https://msdn.microsoft.com/ecb39bac-f062-4835-bbae-f9f643ffde9b">WaitForNtmsNotification</a>
 

 

