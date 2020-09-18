---
UID: NF:ktmw32.RollbackTransactionAsync
title: RollbackTransactionAsync function (ktmw32.h)
description: Requests that the specified transaction be rolled back. This function returns asynchronously.
helpviewer_keywords: ["RollbackTransactionAsync","RollbackTransactionAsync function [Files]","fs.rollbacktransactionasync","ktmw32/RollbackTransactionAsync"]
old-location: fs\rollbacktransactionasync.htm
tech.root: fs
ms.assetid: df23e5af-c37e-4e60-b160-6ffa8f6a26e3
ms.date: 12/05/2018
ms.keywords: RollbackTransactionAsync, RollbackTransactionAsync function [Files], fs.rollbacktransactionasync, ktmw32/RollbackTransactionAsync
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RollbackTransactionAsync
 - ktmw32/RollbackTransactionAsync
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ktmw32.dll
api_name:
 - RollbackTransactionAsync
---

# RollbackTransactionAsync function


## -description

Requests that the specified transaction be rolled back.  This function returns asynchronously.

## -parameters

### -param TransactionHandle [in]

A handle to the transaction.

## -returns

If the function succeeds, the return value is nonzero, and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_IO_PENDING.

If the function fails, the return value is zero. To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-committransaction">CommitTransaction</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-opentransaction">OpenTransaction</a>