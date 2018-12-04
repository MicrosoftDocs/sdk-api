---
UID: NF:wnvapi.WnvRequestNotification
title: WnvRequestNotification function
author: windows-sdk-content
description: Requests notification from the Windows Network Virtualization (WNV) driver whenever a certain type of event occurs.
old-location: wnv\wnvrequestnotification.htm
tech.root: wnv
ms.assetid: CA0F9AAE-95E5-4A62-8A26-11F933B2D09E
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WnvRequestNotification, WnvRequestNotification function [Windows Network Virtualization], wnv.wnvrequestnotification, wnvapi/WnvRequestNotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wnvapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Wnvapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wnvapi.dll
api_name:
 - WnvRequestNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WnvRequestNotification function


## -description


Requests notification from the Windows Network Virtualization (WNV) driver whenever a certain type of event occurs.


## -parameters




### -param WnvHandle

Type: <b>HANDLE</b>

An object handle that is returned from a call to the <a href="https://msdn.microsoft.com/C20BA303-7ECD-4CF3-BB5E-D4509162CD85">WnvOpen</a> function.


### -param NotificationParam

Type: <b><a href="https://msdn.microsoft.com/C8A27B21-462A-4D70-AA19-743023FD1810">PWNV_NOTIFICATION_PARAM</a></b>

A pointer to the notification type for the request.


### -param Overlapped

Type: <b><a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">LPOVERLAPPED</a></b>

Information about the asynchronous completion of this request. If this parameter is <b>NULL</b>, the request is synchronous.


### -param BytesTransferred

Type: <b>PULONG</b>

When this function returns, the <i>BytesTransferred</i> parameter points to the size of the buffer that is filled with the notification structures of the specific event type.


## -returns



Type: <b>ULONG</b>

If the operation succeeds, the function returns <b>ERROR_SUCCESS</b>.

If the operation fails, the function returns one of the following system error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
There is a problem with the <i>NotificationParam</i> parameter, in the <a href="https://msdn.microsoft.com/C8A27B21-462A-4D70-AA19-743023FD1810">WNV_NOTIFICATION_PARAM</a> structure's <b>Header</b> field:

<ul>
<li>The major and minor version values of the <a href="https://msdn.microsoft.com/3D139C56-0224-4120-B308-A33F257DD9DC">WNV_OBJECT_HEADER</a>   structure are incorrect</li>
<li>The size specified in the <a href="https://msdn.microsoft.com/3D139C56-0224-4120-B308-A33F257DD9DC">WNV_OBJECT_HEADER</a>   structure is smaller than at least one notification structure of these types:<ul>
<li>
<a href="https://msdn.microsoft.com/12FF591A-B696-49DF-9E75-B966569A2AAE">WNV_OBJECT_CHANGE_PARAM</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2781B0D6-950E-49AD-9B30-31DE4A27ED4A">WNV_POLICY_MISMATCH_PARAM</a>
</li>
<li>
<a href="https://msdn.microsoft.com/53305594-4539-490E-B034-99355265F175">WNV_REDIRECT_PARAM</a>
</li>
</ul>
</li>
</ul>
</td>
</tr>
</table>
 




## -remarks



This function can be called synchronously or asynchronously.

Three notification types are defined in the <a href="https://msdn.microsoft.com/C8A27B21-462A-4D70-AA19-743023FD1810">WNV_NOTIFICATION_PARAM</a> structure. Each call to this function can request only one type of notification. To receive multiple notification types, the process must make one call for each notification on the same handle. The WNV driver returns at least one notification of the type specified in each call when the notification events occur.



