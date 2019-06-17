---
UID: NF:ntmsapi.CloseNtmsNotification
title: CloseNtmsNotification function (ntmsapi.h)
author: windows-sdk-content
description: The CloseNtmsNotification function closes the specified open notification channel.
old-location: fs\closentmsnotification.htm
tech.root: Rsm
ms.assetid: 30aa06af-70d4-45c0-b624-575dcf867efb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CloseNtmsNotification, CloseNtmsNotification function [Files], _zaw_closentmsnotification, base.closentmsnotification, fs.closentmsnotification, ntmsapi/CloseNtmsNotification
ms.topic: function
f1_keywords: ["ntmsapi/CloseNtmsNotification"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - CloseNtmsNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CloseNtmsNotification function


## -description


<p class="CCE_Message">[<a href="https://docs.microsoft.com/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>CloseNtmsNotification</b> function closes the specified open notification channel.


## -parameters




### -param hNotification [in]

Notification handle returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmsnotification">OpenNtmsNotification</a> function.


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
<a href="https://docs.microsoft.com/windows/desktop/api/ntmsapi/nf-ntmsapi-waitforntmsnotification">WaitForNtmsNotification</a> function, an error returns.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Database Notification Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmsnotification">OpenNtmsNotification</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntmsapi/nf-ntmsapi-waitforntmsnotification">WaitForNtmsNotification</a>
 

 

