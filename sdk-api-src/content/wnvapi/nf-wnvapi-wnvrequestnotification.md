---
UID: NF:wnvapi.WnvRequestNotification
title: WnvRequestNotification function (wnvapi.h)
description: Requests notification from the Windows Network Virtualization (WNV) driver whenever a certain type of event occurs.
old-location: wnv\wnvrequestnotification.htm
tech.root: wnv
ms.assetid: CA0F9AAE-95E5-4A62-8A26-11F933B2D09E
ms.date: 12/05/2018
ms.keywords: WnvRequestNotification, WnvRequestNotification function [Windows Network Virtualization], wnv.wnvrequestnotification, wnvapi/WnvRequestNotification
ms.topic: function
f1_keywords:
- wnvapi/WnvRequestNotification
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WnvRequestNotification function


## -description


Requests notification from the Windows Network Virtualization (WNV) driver whenever a certain type of event occurs.


## -parameters




### -param WnvHandle

Type: <b>HANDLE</b>

An object handle that is returned from a call to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wnvapi/nf-wnvapi-wnvopen">WnvOpen</a> function.


### -param NotificationParam

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/wnvapi/ns-wnvapi-wnv_notification_param">PWNV_NOTIFICATION_PARAM</a></b>

A pointer to the notification type for the request.


### -param Overlapped

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">LPOVERLAPPED</a></b>

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
There is a problem with the <i>NotificationParam</i> parameter, in the <a href="https://docs.microsoft.com/windows/desktop/api/wnvapi/ns-wnvapi-wnv_notification_param">WNV_NOTIFICATION_PARAM</a> structure's <b>Header</b> field:

<ul>
<li>The major and minor version values of the <a href="https://docs.microsoft.com/windows/desktop/api/wnvapi/ns-wnvapi-wnv_object_header">WNV_OBJECT_HEADER</a>   structure are incorrect</li>
<li>The size specified in the <a href="https://docs.microsoft.com/windows/desktop/api/wnvapi/ns-wnvapi-wnv_object_header">WNV_OBJECT_HEADER</a>   structure is smaller than at least one notification structure of these types:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wnvapi/ns-wnvapi-wnv_object_change_param">WNV_OBJECT_CHANGE_PARAM</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wnvapi/ns-wnvapi-wnv_policy_mismatch_param">WNV_POLICY_MISMATCH_PARAM</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wnvapi/ns-wnvapi-wnv_redirect_param">WNV_REDIRECT_PARAM</a>
</li>
</ul>
</li>
</ul>
</td>
</tr>
</table>
 




## -remarks



This function can be called synchronously or asynchronously.

Three notification types are defined in the <a href="https://docs.microsoft.com/windows/desktop/api/wnvapi/ns-wnvapi-wnv_notification_param">WNV_NOTIFICATION_PARAM</a> structure. Each call to this function can request only one type of notification. To receive multiple notification types, the process must make one call for each notification on the same handle. The WNV driver returns at least one notification of the type specified in each call when the notification events occur.



