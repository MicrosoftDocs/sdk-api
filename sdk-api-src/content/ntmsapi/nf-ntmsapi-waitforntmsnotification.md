---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WaitForNtmsNotification function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>WaitForNtmsNotification</b> function waits for the next object change notification.


## -parameters




### -param hNotification [in]

Notification handle returned by the 
<a href="https://msdn.microsoft.com/a5b6ab4a-ab4c-4c84-877f-824dc9ac19a7">OpenNtmsNotification</a> function.


### -param lpNotificationInformation [out]

Pointer to an 
<a href="https://msdn.microsoft.com/d9c6904b-260d-4598-9575-49c7d7b6e66d">NTMS_NOTIFICATIONINFORMATION</a> structure that receives the notification information.


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




<a href="https://msdn.microsoft.com/30aa06af-70d4-45c0-b624-575dcf867efb">CloseNtmsNotification</a>



<a href="removable_storage_manager_functions.htm">Database Notification Functions</a>



<a href="https://msdn.microsoft.com/d9c6904b-260d-4598-9575-49c7d7b6e66d">NTMS_NOTIFICATIONINFORMATION</a>



<a href="https://msdn.microsoft.com/a5b6ab4a-ab4c-4c84-877f-824dc9ac19a7">OpenNtmsNotification</a>
 

 

