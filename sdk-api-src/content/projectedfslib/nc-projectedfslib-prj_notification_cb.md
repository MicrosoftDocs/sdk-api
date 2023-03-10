---
UID: NC:projectedfslib.PRJ_NOTIFICATION_CB
title: PRJ_NOTIFICATION_CB (projectedfslib.h)
description: Delivers notifications to the provider about file system operations.
helpviewer_keywords: ["PRJ_NOTIFICATION_CB","PRJ_NOTIFICATION_CB callback","PRJ_NOTIFICATION_CB callback function","ProjFS.prj_notification_cb","projectedfslib/PRJ_NOTIFICATION_CB"]
old-location: projfs\prj_notification_cb.htm
tech.root: ProjFS
ms.assetid: 7F149A78-2668-4BF2-88D3-1E40CA469AA6
ms.date: 12/05/2018
ms.keywords: PRJ_NOTIFICATION_CB, PRJ_NOTIFICATION_CB callback, PRJ_NOTIFICATION_CB callback function, ProjFS.prj_notification_cb, projectedfslib/PRJ_NOTIFICATION_CB
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - PRJ_NOTIFICATION_CB
 - projectedfslib/PRJ_NOTIFICATION_CB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - projectedfslib.h
api_name:
 - PRJ_NOTIFICATION_CB
---

# PRJ_NOTIFICATION_CB callback function


## -description

Delivers notifications to the provider about file system operations.

## -parameters

### -param callbackData [in]

Information about the operation. The following <i>callbackData</i> members are necessary to implement this callback:<dl>
<dd><b>FilePathName</b> Identifies the path for the file or directory to which the notification pertains.

</dd>
</dl>


The provider can access this buffer only while the callback is running. If it wishes to pend the operation and it requires data from this buffer, it must make its own copy of it.

### -param isDirectory [in]

TRUE if the <b>FilePathName</b> field in <i>callbackData</i> refers to a directory, FALSE otherwise.

### -param notification [in]

A <a href="/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification">PRJ_NOTIFICATION</a> value specifying the notification.

### -param destinationFileName [in, optional]

If <b>notification</b> is <b>PRJ_NOTIFICATION_PRE_RENAME </b> or <b>PRJ_NOTIFICATION_PRE_SET_HARDLINK</b>, this points to a null-terminated Unicode string specifying the path, relative to the virtualization root, of the target of the rename or set-hardlink operation.

### -param operationParameters [in, out]

A pointer to a <a href="/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_parameters">PRJ_NOTIFICATION_PARAMETERS</a> union specifying extra parameters for certain values of <i>notification</i>:

<b>PRJ_NOTIFICATION_FILE_OPENED</b>, <b>PRJ_NOTIFICATION_NEW_FILE_CREATED</b>, or <b>PRJ_NOTIFICATION_FILE_OVERWRITTEN</b><dl>
<dd>
The fields of the <b>PostCreate</b> member are specified.  These fields are:

<b>NotificationMask</b><dl>
<dd>
Upon return from the PRJ_NOTIFICATION_CB callback, the provider may specify a new set of notifications that it wishes to receive for the file here. 

If the provider sets this value to 0, it is equivalent to specifying <b>PRJ_NOTIFY_USE_EXISTING_MASK</b>.

</dd>
</dl>


</dd>
</dl>


<b>PRJ_NOTIFICATION_FILE_RENAMED</b><dl>
<dd>
The fields of the <b>FileRenamed</b> member are specified.  These fields are:

<b>NotificationMask</b><dl>
<dd>
Upon return from the PRJ_NOTIFICATION_CB callback, the provider may specify a new set of notifications that it wishes to receive for the file here. 

If the provider sets this value to 0, it is equivalent to specifying <b>PRJ_NOTIFY_USE_EXISTING_MASK</b>.

</dd>
</dl>


</dd>
</dl>


<b>PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED</b><ul>
<li>
The fields of the <b>FileDeletedOnHandleClose</b> member are specified.  These fields are:

<b>NotificationMask</b><dl>
<dd>
If the provider registered for <b>PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_MODIFIED</b> as well as <b>PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED</b>, this field is set to TRUE if the file was modified before it was deleted.

</dd>
</dl>


</li>
</ul>

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The provider successfully processed the notification.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> 
HRESULT_FROM_WIN32(ERROR_IO_PENDING)</b></dt>
</dl>
</td>
<td width="60%">
The provider wishes to complete the operation at a later time. 


</td>
</tr>
</table>
 

 
An appropriate HRESULT error code if the provider fails the operation. For pre-operation notifications (operations with "PRE" in their name), if the provider returns a failure code ProjFS will fail the corresponding operation with the provided error code.

## -remarks

This callback is optional. If the provider does not supply an implementation of this callback, it will not receive notifications. 


The provider registers for the notifications it wishes to receive when it calls <a href="/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing">PrjStartVirtualizing</a>.