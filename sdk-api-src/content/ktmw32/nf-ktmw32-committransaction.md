---
UID: NF:ktmw32.CommitTransaction
title: CommitTransaction function (ktmw32.h)
description: Requests that the specified transaction be committed. (CommitTransaction)
helpviewer_keywords: ["CommitTransaction","CommitTransaction function [Files]","fs.committransaction","ktmw32/CommitTransaction"]
old-location: fs\committransaction.htm
tech.root: fs
ms.assetid: 17db5e1f-685b-46f0-bac6-dff4c18bb515
ms.date: 12/05/2018
ms.keywords: CommitTransaction, CommitTransaction function [Files], fs.committransaction, ktmw32/CommitTransaction
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
 - CommitTransaction
 - ktmw32/CommitTransaction
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
 - CommitTransaction
---

# CommitTransaction function


## -description

Requests that the specified transaction be committed.

## -parameters

### -param TransactionHandle [in]

A handle to the transaction to be committed. 

This handle must have been opened with the TRANSACTION_COMMIT access right. For more information, see <a href="/windows/desktop/Ktm/ktm-security-and-access-rights">KTM Security and Access Rights</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

The following list identifies the possible error codes:

## -remarks

You can commit any transaction handle that has been opened or created using the TRANSACTION_COMMIT permission; any application can commit a transaction, not just the creator.

This function can only be called if the transaction is still active, not prepared, pre-prepared, or rolled back.

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-opentransaction">OpenTransaction</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-rollbacktransaction">RollbackTransaction</a>
