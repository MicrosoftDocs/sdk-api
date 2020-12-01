---
UID: NS:ktmtypes._TRANSACTION_NOTIFICATION
title: TRANSACTION_NOTIFICATION (ktmtypes.h)
description: Contains the data that is associated with a transaction notification.
helpviewer_keywords: ["*PTRANSACTION_NOTIFICATION","PTRANSACTION_NOTIFICATION","PTRANSACTION_NOTIFICATION structure pointer [Files]","TRANSACTION_NOTIFICATION","TRANSACTION_NOTIFICATION structure [Files]","fs.transaction_notification","ktmtypes/PTRANSACTION_NOTIFICATION","ktmtypes/TRANSACTION_NOTIFICATION"]
old-location: fs\transaction_notification.htm
tech.root: fs
ms.assetid: 4f87de9d-a068-4ab9-8f38-b75f20552b1d
ms.date: 12/05/2018
ms.keywords: '*PTRANSACTION_NOTIFICATION, PTRANSACTION_NOTIFICATION, PTRANSACTION_NOTIFICATION structure pointer [Files], TRANSACTION_NOTIFICATION, TRANSACTION_NOTIFICATION structure [Files], fs.transaction_notification, ktmtypes/PTRANSACTION_NOTIFICATION, ktmtypes/TRANSACTION_NOTIFICATION'
req.header: ktmtypes.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TRANSACTION_NOTIFICATION, *PTRANSACTION_NOTIFICATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TRANSACTION_NOTIFICATION
 - ktmtypes/_TRANSACTION_NOTIFICATION
 - PTRANSACTION_NOTIFICATION
 - ktmtypes/PTRANSACTION_NOTIFICATION
 - TRANSACTION_NOTIFICATION
 - ktmtypes/TRANSACTION_NOTIFICATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - KtmTypes.h
api_name:
 - TRANSACTION_NOTIFICATION
---

# TRANSACTION_NOTIFICATION structure


## -description

Contains the data that is associated with a transaction notification.

## -struct-fields

### -field TransactionKey

The user-defined, opaque ID for this transaction.

### -field TransactionNotification

The <a href="/windows/desktop/Ktm/notification-mask">NOTIFICATION_MASK</a> value for this 
      transaction.

### -field TmVirtualClock

The latest virtual clock value that is associated with this transaction. See 
      <a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a>.

### -field ArgumentLength

Indicates the number of bytes for the 
      <a href="/windows/win32/api/ktmtypes/ns-ktmtypes-transaction_notification_recovery_argument">TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT</a> 
      structure that follow this 
      <b>TRANSACTION_NOTIFICATION</b> structure.

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-createenlistment">CreateEnlistment</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-getnotificationresourcemanager">GetNotificationResourceManager</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-getnotificationresourcemanagerasync">GetNotificationResourceManagerAsync</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-structures">Kernel Transaction Manager Structures</a>



<a href="/windows/desktop/Ktm/notification-mask">NOTIFICATION_MASK</a>



<a href="/windows/win32/api/ktmtypes/ns-ktmtypes-transaction_notification_recovery_argument">TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT</a>