---
UID: NF:ktmw32.SetTransactionInformation
title: SetTransactionInformation function
author: windows-sdk-content
description: Sets the transaction information for the specified transaction.
old-location: fs\settransactioninformation.htm
old-project: Ktm
ms.assetid: e33d221b-cd06-4f20-a4b5-407a04362ba0
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: SetTransactionInformation, SetTransactionInformation function [Files], fs.settransactioninformation, ktmw32/SetTransactionInformation
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT, *PTRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ktmw32.dll
api_name:
 - SetTransactionInformation
product: Windows
targetos: Windows
req.lib: Ktmw32.lib
req.dll: Ktmw32.dll
req.irql: 
req.product: GDI+ 1.1
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
 

 

