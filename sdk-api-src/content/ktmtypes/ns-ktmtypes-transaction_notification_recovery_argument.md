---
UID: NS:ktmtypes._TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT
title: TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT (ktmtypes.h)
author: windows-sdk-content
description: Indicates the transaction to be recovered. This structure is sent with a recovery notification.
old-location: fs\transaction_notification_recovery_argument.htm
tech.root: ktm
ms.assetid: 29a32b89-22d1-4d26-8927-a2051dd5d37a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PTRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT, PTRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT, PTRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT structure [Files], TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT, TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT structure [Files], fs.transaction_notification_recovery_argument, ktmtypes/PTRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT, ktmtypes/TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT"
ms.topic: struct
f1_keywords: 
 - "ktmtypes/TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - KtmTypes.h
api_name:
 - TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT
product: Windows
targetos: Windows
req.typenames: TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT, *PTRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT
req.redist: 
ms.custom: 19H1
---

# TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT structure


## -description


Indicates the transaction  to be recovered. This structure is sent with a recovery notification.


## -struct-fields




### -field EnlistmentId

The enlistment identifier.


### -field UOW

The transaction identifier, sometimes called the unit of work.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-getnotificationresourcemanager">GetNotificationResourceManager</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-getnotificationresourcemanagerasync">GetNotificationResourceManagerAsync</a>



<a href="https://docs.microsoft.com/windows/desktop/Ktm/kernel-transaction-manager-structures">Kernel Transaction Manager Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ktmtypes/ns-ktmtypes-_transaction_notification">TRANSACTION_NOTIFICATION</a>
 

 

