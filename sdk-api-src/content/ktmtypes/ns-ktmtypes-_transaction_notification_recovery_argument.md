---
UID: NS:ktmtypes._TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT
title: "_TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT"
author: windows-sdk-content
description: Indicates the transaction to be recovered. This structure is sent with a recovery notification.
old-location: fs\transaction_notification_recovery_argument.htm
tech.root: ktm
ms.assetid: 29a32b89-22d1-4d26-8927-a2051dd5d37a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PTRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT, PTRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT, PTRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT structure [Files], TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT, TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT structure [Files], _TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT, fs.transaction_notification_recovery_argument, ktmtypes/PTRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT, ktmtypes/TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
---

# _TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT structure


## -description


Indicates the transaction  to be recovered. This structure is sent with a recovery notification.


## -struct-fields




### -field EnlistmentId

The enlistment identifier.


### -field UOW

The transaction identifier, sometimes called the unit of work.


## -see-also




<a href="https://msdn.microsoft.com/d606f960-e843-4478-8ba7-5201f85c44ce">GetNotificationResourceManager</a>



<a href="https://msdn.microsoft.com/c83e104b-6cd7-4399-8232-7c2e7b408f1a">GetNotificationResourceManagerAsync</a>



<a href="https://msdn.microsoft.com/74976925-1813-4dbd-9438-26fabd704d84">Kernel Transaction Manager Structures</a>



<a href="https://msdn.microsoft.com/4f87de9d-a068-4ab9-8f38-b75f20552b1d">TRANSACTION_NOTIFICATION</a>
 

 

