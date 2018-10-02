---
UID: NF:ktmw32.RollbackTransactionAsync
title: RollbackTransactionAsync function
author: windows-sdk-content
description: Requests that the specified transaction be rolled back. This function returns asynchronously.
old-location: fs\rollbacktransactionasync.htm
tech.root: Ktm
ms.assetid: df23e5af-c37e-4e60-b160-6ffa8f6a26e3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RollbackTransactionAsync, RollbackTransactionAsync function [Files], fs.rollbacktransactionasync, ktmw32/RollbackTransactionAsync
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
req.lib: Ktmw32.lib
req.dll: Ktmw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ktmw32.dll
api_name:
 - RollbackTransactionAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RollbackTransactionAsync function


## -description


Requests that the specified transaction be rolled back.  This function returns asynchronously.


## -parameters




### -param TransactionHandle [in]

A handle to the transaction.


## -returns



If the function succeeds, the return value is nonzero, and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_IO_PENDING.

If the function fails, the return value is zero. To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. The following list identifies the possible error codes: 




## -see-also




<a href="https://msdn.microsoft.com/17db5e1f-685b-46f0-bac6-dff4c18bb515">CommitTransaction</a>



<a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>



<a href="https://msdn.microsoft.com/d95f15e4-d0fd-4665-849d-eecac8fc542b">OpenTransaction</a>
 

 

