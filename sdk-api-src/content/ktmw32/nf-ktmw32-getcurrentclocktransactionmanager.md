---
UID: NF:ktmw32.GetCurrentClockTransactionManager
title: GetCurrentClockTransactionManager function (ktmw32.h)
description: Obtains a virtual clock value from a transaction manager.
helpviewer_keywords: ["GetCurrentClockTransactionManager","GetCurrentClockTransactionManager function [Files]","fs.getcurrentclocktransactionmanager_func","ktmw32/GetCurrentClockTransactionManager"]
old-location: fs\getcurrentclocktransactionmanager_func.htm
tech.root: fs
ms.assetid: 21d7c0fa-3a49-43b3-9325-d3dfdabbcb98
ms.date: 12/05/2018
ms.keywords: GetCurrentClockTransactionManager, GetCurrentClockTransactionManager function [Files], fs.getcurrentclocktransactionmanager_func, ktmw32/GetCurrentClockTransactionManager
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
 - GetCurrentClockTransactionManager
 - ktmw32/GetCurrentClockTransactionManager
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
 - GetCurrentClockTransactionManager
---

# GetCurrentClockTransactionManager function


## -description

Obtains a virtual clock value from a transaction manager.

## -parameters

### -param TransactionManagerHandle [in]

A handle to the transaction manager to obtain a virtual clock value for.

### -param TmVirtualClock [out]

The latest virtual clock value for the transaction manager. See <a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.


The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-commitcomplete">CommitComplete</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-preparecomplete">PrepareComplete</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-prepreparecomplete">PreprepareComplete</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-readonlyenlistment">ReadOnlyEnlistment</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-rollbackcomplete">RollbackComplete</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-rollbackenlistment">RollbackEnlistment</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-singlephasereject">SinglePhaseReject</a>