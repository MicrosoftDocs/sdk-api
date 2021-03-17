---
UID: NF:ktmw32.RollbackTransaction
title: RollbackTransaction function (ktmw32.h)
description: Requests that the specified transaction be rolled back.
helpviewer_keywords: ["RollbackTransaction","RollbackTransaction function [Files]","fs.rollbacktransaction","ktmw32/RollbackTransaction"]
old-location: fs\rollbacktransaction.htm
tech.root: fs
ms.assetid: 7d3522b8-ddf0-449e-8ab4-09e679ba1f15
ms.date: 12/05/2018
ms.keywords: RollbackTransaction, RollbackTransaction function [Files], fs.rollbacktransaction, ktmw32/RollbackTransaction
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
 - RollbackTransaction
 - ktmw32/RollbackTransaction
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
 - RollbackTransaction
---

# RollbackTransaction function


## -description

        Requests that the specified transaction be rolled back.  This function is synchronous.

## -parameters

### -param TransactionHandle [in]

A handle to the transaction.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-committransaction">CommitTransaction</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-opentransaction">OpenTransaction</a>