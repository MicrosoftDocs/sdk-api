---
UID: NF:ktmw32.GetNotificationResourceManager
title: GetNotificationResourceManager function (ktmw32.h)
description: Requests and receives a notification for a resource manager (RM). This function is used by the RM register to receive notifications when a transaction changes state.
helpviewer_keywords: ["GetNotificationResourceManager","GetNotificationResourceManager function [Files]","fs.getnotificationresourcemanager","ktmw32/GetNotificationResourceManager"]
old-location: fs\getnotificationresourcemanager.htm
tech.root: fs
ms.assetid: d606f960-e843-4478-8ba7-5201f85c44ce
ms.date: 12/05/2018
ms.keywords: GetNotificationResourceManager, GetNotificationResourceManager function [Files], fs.getnotificationresourcemanager, ktmw32/GetNotificationResourceManager
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
req.lib: KtmW32.lib
req.dll: KtmW32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetNotificationResourceManager
 - ktmw32/GetNotificationResourceManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - KtmW32.dll
api_name:
 - GetNotificationResourceManager
---

# GetNotificationResourceManager function


## -description

Requests and receives a notification for a resource manager (RM). This function is used by the RM 
    register to receive notifications when a transaction changes state.

## -parameters

### -param ResourceManagerHandle [in]

A handle  to the resource manager.

### -param TransactionNotification [out]

A pointer to a <a href="/windows/desktop/api/ktmtypes/ns-ktmtypes-transaction_notification">TRANSACTION_NOTIFICATION</a> 
      structure that receives the first available notification.

### -param NotificationLength [in]

The size of the <i>TransactionNotification</i> buffer, in bytes.

### -param dwMilliseconds [in, optional]

The time, in milliseconds, for which the calling application is blocking while waiting for the notification 
      to become available. If no notifications are available when the timeout expires, 
      <b>ERROR_TIMEOUT</b> is returned.

### -param ReturnLength [out, optional]

A pointer to a variable that receives the actual size of the notification received by the 
      <i>TransactionNotification</i> parameter.

## -returns

If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero (0). To get extended error information, call the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

 The following list identifies the possible error codes:

## -remarks

All resource managers must register to receive <b>TRANSACTION_NOTIFY_PREPREPARE</b>, 
     <b>TRANSACTION_NOTIFY_PREPARE</b>, and <b>TRANSACTION_NOTIFY_COMMIT</b> 
     notifications, even if they subsequently call 
     <a href="/windows/desktop/api/ktmw32/nf-ktmw32-readonlyenlistment">ReadOnlyEnlistment</a> to mark an enlistment as 
     read-only. Resource managers can support <b>TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT</b>, but 
     they must also support the multi-phase pre-prepare, prepare, and commit notifications. For the list of all 
     notifications that resource managers can receive, see 
     <a href="/windows/desktop/api/ktmtypes/ns-ktmtypes-transaction_notification">TRANSACTION_NOTIFICATION</a>.

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-createenlistment">CreateEnlistment</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-getnotificationresourcemanagerasync">GetNotificationResourceManagerAsync</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/Ktm/notification-mask">NOTIFICATION_MASK</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-setresourcemanagercompletionport">SetResourceManagerCompletionPort</a>



<a href="/windows/desktop/api/ktmtypes/ns-ktmtypes-transaction_notification">TRANSACTION_NOTIFICATION</a>



<a href="/windows/win32/api/ktmtypes/ns-ktmtypes-transaction_notification_recovery_argument">TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT</a>