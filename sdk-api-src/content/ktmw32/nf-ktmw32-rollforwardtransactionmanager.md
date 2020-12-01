---
UID: NF:ktmw32.RollforwardTransactionManager
title: RollforwardTransactionManager function (ktmw32.h)
description: Recovers information only to the specified virtual clock value.
helpviewer_keywords: ["RollforwardTransactionManager","RollforwardTransactionManager function [Files]","fs.rollforwardtransactionmanager","ktmw32/RollforwardTransactionManager"]
old-location: fs\rollforwardtransactionmanager.htm
tech.root: fs
ms.assetid: 13492b74-8707-46bb-93f1-59c3c5ceab6d
ms.date: 12/05/2018
ms.keywords: RollforwardTransactionManager, RollforwardTransactionManager function [Files], fs.rollforwardtransactionmanager, ktmw32/RollforwardTransactionManager
req.header: ktmw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
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
req.lib: KtmW32.lib
req.dll: KtmW32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RollforwardTransactionManager
 - ktmw32/RollforwardTransactionManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - KtmW32.dll
api_name:
 - RollforwardTransactionManager
---

# RollforwardTransactionManager function


## -description

Recovers information only to the specified virtual clock value.

## -parameters

### -param TransactionManagerHandle [in]

A handle to the transaction manager.

### -param TmVirtualClock [in]

A pointer to the latest virtual clock value received for this transaction.

## -returns

If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is 0 (zero). To get extended error information, call the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-getcurrentclocktransactionmanager">GetCurrentClockTransactionManager</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>