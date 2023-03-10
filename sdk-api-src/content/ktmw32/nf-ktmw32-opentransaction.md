---
UID: NF:ktmw32.OpenTransaction
title: OpenTransaction function (ktmw32.h)
description: Opens an existing transaction.
helpviewer_keywords: ["OpenTransaction","OpenTransaction function [Files]","fs.opentransaction","ktmw32/OpenTransaction"]
old-location: fs\opentransaction.htm
tech.root: fs
ms.assetid: d95f15e4-d0fd-4665-849d-eecac8fc542b
ms.date: 12/05/2018
ms.keywords: OpenTransaction, OpenTransaction function [Files], fs.opentransaction, ktmw32/OpenTransaction
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
 - OpenTransaction
 - ktmw32/OpenTransaction
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
 - OpenTransaction
---

# OpenTransaction function


## -description

Opens an existing transaction.

## -parameters

### -param dwDesiredAccess [in]

The access to the transaction object. You must have read and write access to work with a transaction. See <a href="/windows/desktop/Ktm/transaction-access-masks">Transaction Access Masks</a> for a list of valid values.

### -param TransactionId [in]

The GUID that identifies the transaction to be opened. This is commonly referred to as  a unit of work for the transaction.

## -returns

If the function succeeds, the return value is a handle to the transaction.

If the function fails, the return value is INVALID_HANDLE_VALUE. To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

The following list identifies the  possible error codes:

## -remarks

Clients close the transaction handle by using the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function. If the last transaction handle is closed without anyone calling the <a href="/windows/desktop/api/ktmw32/nf-ktmw32-committransaction">CommitTransaction</a> function on the transaction, then the KTM implicitly rolls back the transaction.

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-committransaction">CommitTransaction</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-rollbacktransaction">RollbackTransaction</a>



<a href="/windows/desktop/Ktm/transaction-access-masks">Transaction Access Masks</a>