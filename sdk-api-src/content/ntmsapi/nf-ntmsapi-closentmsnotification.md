---
UID: NF:ntmsapi.CloseNtmsNotification
title: CloseNtmsNotification function
author: windows-driver-content
description: The CloseNtmsNotification function closes the specified open notification channel.
old-location: fs\closentmsnotification.htm
old-project: Rsm
ms.assetid: 30aa06af-70d4-45c0-b624-575dcf867efb
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: CloseNtmsNotification, CloseNtmsNotification function [Files], _zaw_closentmsnotification, base.closentmsnotification, fs.closentmsnotification, ntmsapi/CloseNtmsNotification
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntmsapi.dll
api_name:
-	CloseNtmsNotification
product: Windows
targetos: Windows
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# CloseNtmsNotification function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>CloseNtmsNotification</b> function closes the specified open notification channel.


## -parameters




### -param hNotification [in]

Notification handle returned by the 
<a href="https://msdn.microsoft.com/a5b6ab4a-ab4c-4c84-877f-824dc9ac19a7">OpenNtmsNotification</a> function.


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
The value specified in the <i>hNotification</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>hNotification</i> parameter is  <b>NULL</b>.

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
</table>
 




## -remarks



If the 
<b>CloseNtmsNotification</b> function is called while there is an outstanding call to the 
<a href="https://msdn.microsoft.com/ecb39bac-f062-4835-bbae-f9f643ffde9b">WaitForNtmsNotification</a> function, an error returns.




## -see-also




<a href="removable_storage_manager_functions.htm">Database Notification Functions</a>



<a href="https://msdn.microsoft.com/a5b6ab4a-ab4c-4c84-877f-824dc9ac19a7">OpenNtmsNotification</a>



<a href="https://msdn.microsoft.com/ecb39bac-f062-4835-bbae-f9f643ffde9b">WaitForNtmsNotification</a>
 

 

