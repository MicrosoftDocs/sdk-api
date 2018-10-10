---
UID: NC:projectedfslib.PRJ_NOTIFICATION_CB
title: PRJ_NOTIFICATION_CB
author: windows-sdk-content
description: Delivers notifications to the provider about file system operations.
old-location: projfs\prj_notification_cb.htm
tech.root: ProjFS
ms.assetid: 7F149A78-2668-4BF2-88D3-1E40CA469AA6
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: PRJ_NOTIFICATION_CB, PRJ_NOTIFICATION_CB callback, PRJ_NOTIFICATION_CB callback function, ProjFS.prj_notification_cb, projectedfslib/PRJ_NOTIFICATION_CB
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - projectedfslib.h
api_name:
 - PRJ_NOTIFICATION_CB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PRJ_NOTIFICATION_CB callback function


## -description


Delivers notifications to the provider about file system operations. 


## -parameters




### -param callbackData [in]

Information about the operation.


### -param isDirectory [in]

TRUE if the FilePathName field in callbackData refers to a directory, FALSE otherwise.


### -param notification [in]

Values specifying the notification.


### -param destinationFileName [in, optional]

If notification is PRJ_NOTIFICATION_PRE_RENAME or PRJ_NOTIFICATION_PRE_SET_HARDLINK, this points to a null-terminated Unicode string specifying the path, relative to the virtualization root, of the target of the rename or set-hardlink operation.


### -param operationParameters [in, out]

Specifies extra notification parameters.


## -returns



S_OK: The provider successfully processed the notification.

 
HRESULT_FROM_WIN32(ERROR_IO_PENDING): The provider wishes to complete the operation at a later time. 
An appropriate HRESULT error code if the provider fails the operation




## -remarks



This callback is optional. If the provider does not supply an implementation of this callback, it will not receive notifications. 


The provider registers for the notifications it wishes to receive when it calls <a href="projfs.prjstartvirtualizing">PrjStartVirtualizing</a>.



