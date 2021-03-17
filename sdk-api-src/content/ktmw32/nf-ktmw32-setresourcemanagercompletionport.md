---
UID: NF:ktmw32.SetResourceManagerCompletionPort
title: SetResourceManagerCompletionPort function (ktmw32.h)
description: Associates the specified I/O completion port with the specified resource manager (RM). This port receives all notifications for the RM.
helpviewer_keywords: ["SetResourceManagerCompletionPort","SetResourceManagerCompletionPort function [Files]","fs.setresourcemanagercompletionport","ktmw32/SetResourceManagerCompletionPort"]
old-location: fs\setresourcemanagercompletionport.htm
tech.root: fs
ms.assetid: 219fc899-84ee-474f-9f86-6ebf9c721810
ms.date: 12/05/2018
ms.keywords: SetResourceManagerCompletionPort, SetResourceManagerCompletionPort function [Files], fs.setresourcemanagercompletionport, ktmw32/SetResourceManagerCompletionPort
req.header: ktmw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ktmw32.lib
req.dll: Ktmw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetResourceManagerCompletionPort
 - ktmw32/SetResourceManagerCompletionPort
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ktmw32.dll
api_name:
 - SetResourceManagerCompletionPort
---

# SetResourceManagerCompletionPort function


## -description

Associates the specified I/O completion port with the specified resource manager (RM). This port receives all notifications for the RM.

## -parameters

### -param ResourceManagerHandle [in]

A handle to the resource manager.

### -param IoCompletionPortHandle [in]

A handle to the I/O completion port.

### -param CompletionKey [in]

The user-defined identifier. Typically, it is used to associate the receive notification with a specific resource manager.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

The following list identifies the possible error codes:

## -remarks

This function must be used in conjunction with the <a href="/windows/desktop/api/ktmw32/nf-ktmw32-getnotificationresourcemanagerasync">GetNotificationResourceManagerAsync</a> function, which provides the buffers that KTM uses to deliver notifications asynchronously. These functions provide a different way to receive notifications from KTM. You can use these two functions instead of the <a href="/windows/desktop/api/ktmw32/nf-ktmw32-getnotificationresourcemanager">GetNotificationResourceManager</a> function.

This function must be called before calling <a href="/windows/desktop/api/ktmw32/nf-ktmw32-getnotificationresourcemanagerasync">GetNotificationResourceManagerAsync</a>.

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-getnotificationresourcemanager">GetNotificationResourceManager</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-getnotificationresourcemanagerasync">GetNotificationResourceManagerAsync</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>