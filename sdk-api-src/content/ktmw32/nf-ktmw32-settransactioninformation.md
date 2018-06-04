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

# SetTransactionInformation function


## -description


Sets the transaction information for the specified transaction.


## -parameters




### -param TransactionHandle [in]

A handle to the transaction. The handle must have the TRANSACTION_SET_INFORMATION permission to set the transaction information.


### -param OPTIONAL

TBD


### -param Description [in, optional]

The user-defined description of this transaction.


#### - IsolationFlags [in, optional]

Reserved.


#### - IsolationLevel [in, optional]

Reserved; specify zero.


#### - Timeout [in, optional]

The timeout value, in milliseconds, for this transaction.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.


The following list identifies the possible error codes:






## -see-also




<a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a>



<a href="https://msdn.microsoft.com/5ce3c96a-629e-49d0-8ec4-f9bf76af99ac">GetTransactionInformation</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>
 

 

