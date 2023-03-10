---
UID: NF:ktmw32.CommitTransactionAsync
title: CommitTransactionAsync function (ktmw32.h)
description: Requests that the specified transaction be committed. (CommitTransactionAsync)
helpviewer_keywords: ["CommitTransactionAsync","CommitTransactionAsync function [Files]","fs.committransactionasync","ktmw32/CommitTransactionAsync"]
old-location: fs\committransactionasync.htm
tech.root: fs
ms.assetid: cc0f4314-e216-490b-a49a-14bb850e0762
ms.date: 12/05/2018
ms.keywords: CommitTransactionAsync, CommitTransactionAsync function [Files], fs.committransactionasync, ktmw32/CommitTransactionAsync
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
 - CommitTransactionAsync
 - ktmw32/CommitTransactionAsync
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
 - CommitTransactionAsync
---

# CommitTransactionAsync function


## -description

Requests that the specified transaction be committed.

## -parameters

### -param TransactionHandle [in]

A handle to the transaction to be committed. 

This handle must have been opened with the TRANSACTION_COMMIT access right. For more information, see <a href="/windows/desktop/Ktm/ktm-security-and-access-rights">KTM Security and Access Rights</a>.

## -returns

If the function succeeds, the return value is nonzero. Success means that the function completed synchronously, and the calling application does not need to wait for pending results.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.


The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-opentransaction">OpenTransaction</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-rollbacktransaction">RollbackTransaction</a>
