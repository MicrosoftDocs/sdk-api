---
UID: NF:ktmw32.GetNotificationResourceManagerAsync
title: GetNotificationResourceManagerAsync function (ktmw32.h)
description: Requests and receives asynchronous notification for a resource manager (RM). This function is used by the RM register to receive notifications when a transaction changes state.
helpviewer_keywords: ["GetNotificationResourceManagerAsync","GetNotificationResourceManagerAsync function [Files]","fs.getnotificationresourcemanagerasync","ktmw32/GetNotificationResourceManagerAsync"]
old-location: fs\getnotificationresourcemanagerasync.htm
tech.root: fs
ms.assetid: c83e104b-6cd7-4399-8232-7c2e7b408f1a
ms.date: 12/05/2018
ms.keywords: GetNotificationResourceManagerAsync, GetNotificationResourceManagerAsync function [Files], fs.getnotificationresourcemanagerasync, ktmw32/GetNotificationResourceManagerAsync
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
 - GetNotificationResourceManagerAsync
 - ktmw32/GetNotificationResourceManagerAsync
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
 - GetNotificationResourceManagerAsync
---

# GetNotificationResourceManagerAsync function


## -description

Requests and receives asynchronous notification for a resource manager (RM). This function is used by 
    the RM register to receive notifications when a transaction changes state.

## -parameters

### -param ResourceManagerHandle [in]

A handle  to the resource manager.

### -param TransactionNotification [out]

A pointer to a 
      <a href="/windows/desktop/api/ktmtypes/ns-ktmtypes-transaction_notification">TRANSACTION_NOTIFICATION</a> structure that 
      receives the first available notification.

### -param TransactionNotificationLength [in]

The size of the <i>TransactionNotification</i> buffer, in bytes.

### -param ReturnLength [out]

A pointer to a variable that receives the actual size of the notification received by the 
      <i>TransactionNotification</i> parameter.

### -param lpOverlapped [in]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that is 
      required for asynchronous operation.

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

Resource managers (RM) may want to call this function more than once to provide multiple buffers for KTM to 
    use when delivering notifications. The number of calls to this function depends on how much load your RM is 
    carrying.

This function must be called after the 
    <a href="/windows/desktop/api/ktmw32/nf-ktmw32-setresourcemanagercompletionport">SetResourceManagerCompletionPort</a> 
     function is called.

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-createenlistment">CreateEnlistment</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/Ktm/notification-mask">NOTIFICATION_MASK</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-setresourcemanagercompletionport">SetResourceManagerCompletionPort</a>



<a href="/windows/desktop/api/ktmtypes/ns-ktmtypes-transaction_notification">TRANSACTION_NOTIFICATION</a>



<a href="/windows/win32/api/ktmtypes/ns-ktmtypes-transaction_notification_recovery_argument">TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT</a>