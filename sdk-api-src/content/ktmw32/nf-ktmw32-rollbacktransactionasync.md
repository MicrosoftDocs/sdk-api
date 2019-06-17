---
UID: NF:ktmw32.RollbackTransactionAsync
title: RollbackTransactionAsync function (ktmw32.h)
author: windows-sdk-content
description: Requests that the specified transaction be rolled back. This function returns asynchronously.
old-location: fs\rollbacktransactionasync.htm
tech.root: ktm
ms.assetid: df23e5af-c37e-4e60-b160-6ffa8f6a26e3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RollbackTransactionAsync, RollbackTransactionAsync function [Files], fs.rollbacktransactionasync, ktmw32/RollbackTransactionAsync
ms.topic: function
f1_keywords: ["ktmw32/RollbackTransactionAsync"]
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
ms.custom: 19H1
---

# RollbackTransactionAsync function


## -description


Requests that the specified transaction be rolled back.  This function returns asynchronously.


## -parameters




### -param TransactionHandle [in]

A handle to the transaction.


## -returns



If the function succeeds, the return value is nonzero, and <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_IO_PENDING.

If the function fails, the return value is zero. To get extended error information, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. The following list identifies the possible error codes: 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-committransaction">CommitTransaction</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a>



<a href="https://docs.microsoft.com/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-opentransaction">OpenTransaction</a>
 

 

