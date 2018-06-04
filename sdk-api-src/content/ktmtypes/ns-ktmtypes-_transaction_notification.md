---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _TRANSACTION_NOTIFICATION structure


## -description


Contains the data that is associated with a transaction notification.


## -struct-fields




### -field TransactionKey

The user-defined, opaque ID for this transaction.


### -field TransactionNotification

The <a href="https://msdn.microsoft.com/65db8ba5-193c-439b-8e8c-6cb4a9bd4efd">NOTIFICATION_MASK</a> value for this 
      transaction.


### -field TmVirtualClock

The latest virtual clock value that is associated with this transaction. See 
      <a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>.


### -field ArgumentLength

Indicates the number of bytes for the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/ff564820">TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT</a> 
      structure that follow this 
      <b>TRANSACTION_NOTIFICATION</b> structure.


## -see-also




<a href="https://msdn.microsoft.com/7bc06468-947f-48ec-8e58-20df58ed93bd">CreateEnlistment</a>



<a href="https://msdn.microsoft.com/d606f960-e843-4478-8ba7-5201f85c44ce">GetNotificationResourceManager</a>



<a href="https://msdn.microsoft.com/c83e104b-6cd7-4399-8232-7c2e7b408f1a">GetNotificationResourceManagerAsync</a>



<a href="https://msdn.microsoft.com/74976925-1813-4dbd-9438-26fabd704d84">Kernel Transaction Manager Structures</a>



<a href="https://msdn.microsoft.com/65db8ba5-193c-439b-8e8c-6cb4a9bd4efd">NOTIFICATION_MASK</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564820">TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT</a>
 

 

