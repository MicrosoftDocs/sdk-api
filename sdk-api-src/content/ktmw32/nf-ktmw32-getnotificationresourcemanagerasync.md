---
UID: NF:ktmw32.GetNotificationResourceManagerAsync
title: GetNotificationResourceManagerAsync function
author: windows-sdk-content
description: Requests and receives asynchronous notification for a resource manager (RM). This function is used by the RM register to receive notifications when a transaction changes state.
old-location: fs\getnotificationresourcemanagerasync.htm
tech.root: ktm
ms.assetid: c83e104b-6cd7-4399-8232-7c2e7b408f1a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetNotificationResourceManagerAsync, GetNotificationResourceManagerAsync function [Files], fs.getnotificationresourcemanagerasync, ktmw32/GetNotificationResourceManagerAsync
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - KtmW32.dll
api_name:
 - GetNotificationResourceManagerAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
      <a href="https://msdn.microsoft.com/4f87de9d-a068-4ab9-8f38-b75f20552b1d">TRANSACTION_NOTIFICATION</a> structure that 
      receives the first available notification.


### -param TransactionNotificationLength [in]

The size of the <i>TransactionNotification</i> buffer, in bytes.


### -param ReturnLength [out]

A pointer to a variable that receives the actual size of the notification received by the 
      <i>TransactionNotification</i> parameter.


### -param lpOverlapped [in]

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that is 
      required for asynchronous operation.


## -returns



If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is zero (0). To get extended error information, call the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

The following list identifies the possible error codes:




## -remarks



All resource managers must register to receive <b>TRANSACTION_NOTIFY_PREPREPARE</b>, 
     <b>TRANSACTION_NOTIFY_PREPARE</b>, and <b>TRANSACTION_NOTIFY_COMMIT</b> 
     notifications, even if they subsequently call 
     <a href="https://msdn.microsoft.com/a6411fad-8ad0-4a31-9e09-0c18dd384634">ReadOnlyEnlistment</a> to mark an enlistment as 
     read-only. Resource managers can support <b>TRANSACTION_NOTIFY_SINGLE_PHASE_COMMIT</b>, but 
     they must also support the multi-phase pre-prepare, prepare, and commit notifications. For the list of all 
     notifications that resource managers can receive, see 
     <a href="https://msdn.microsoft.com/4f87de9d-a068-4ab9-8f38-b75f20552b1d">TRANSACTION_NOTIFICATION</a>.

Resource managers (RM) may want to call this function more than once to provide multiple buffers for KTM to 
    use when delivering notifications. The number of calls to this function depends on how much load your RM is 
    carrying.

This function must be called after the 
    <a href="https://msdn.microsoft.com/219fc899-84ee-474f-9f86-6ebf9c721810">SetResourceManagerCompletionPort</a> 
     function is called.




## -see-also




<a href="https://msdn.microsoft.com/7bc06468-947f-48ec-8e58-20df58ed93bd">CreateEnlistment</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>



<a href="https://msdn.microsoft.com/65db8ba5-193c-439b-8e8c-6cb4a9bd4efd">NOTIFICATION_MASK</a>



<a href="https://msdn.microsoft.com/219fc899-84ee-474f-9f86-6ebf9c721810">SetResourceManagerCompletionPort</a>



<a href="https://msdn.microsoft.com/4f87de9d-a068-4ab9-8f38-b75f20552b1d">TRANSACTION_NOTIFICATION</a>



<a href="https://msdn.microsoft.com/29a32b89-22d1-4d26-8927-a2051dd5d37a">TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT</a>
 

 

