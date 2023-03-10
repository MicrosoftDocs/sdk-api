---
UID: NF:ktmw32.RollbackEnlistment
title: RollbackEnlistment function (ktmw32.h)
description: Rolls back the specified transaction that is associated with an enlistment. This function cannot be called for read-only enlistments.
helpviewer_keywords: ["RollbackEnlistment","RollbackEnlistment function [Files]","fs.rollbackenlistment","ktmw32/RollbackEnlistment"]
old-location: fs\rollbackenlistment.htm
tech.root: fs
ms.assetid: e62c0c81-6802-4a76-94bb-617933490e83
ms.date: 12/05/2018
ms.keywords: RollbackEnlistment, RollbackEnlistment function [Files], fs.rollbackenlistment, ktmw32/RollbackEnlistment
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
 - RollbackEnlistment
 - ktmw32/RollbackEnlistment
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
 - RollbackEnlistment
---

# RollbackEnlistment function


## -description

Rolls back the specified transaction that is associated with an enlistment. This function cannot be called for read-only enlistments.

## -parameters

### -param EnlistmentHandle [in]

A handle to the enlistment.

### -param TmVirtualClock [in]

The latest virtual clock value received for this enlistment. See <a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a>.

## -returns

If the function succeeds, the return value is nonzero. 


  

If the function fails, the return value is zero (0). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

 The following list identifies the possible error codes:

## -remarks

This function is used by an RM to roll back a transaction in which it is enlisted. All work associated with the transaction is rolled back. 

Rollbacks are allowed by enlistments at any time before it issues a prepare complete notification.

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-getcurrentclocktransactionmanager">GetCurrentClockTransactionManager</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-readonlyenlistment">ReadOnlyEnlistment</a>