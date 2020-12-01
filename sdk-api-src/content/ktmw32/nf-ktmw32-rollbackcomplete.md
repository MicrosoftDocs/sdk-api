---
UID: NF:ktmw32.RollbackComplete
title: RollbackComplete function (ktmw32.h)
description: Indicates that the resource manager (RM) has successfully completed rolling back a transaction.
helpviewer_keywords: ["RollbackComplete","RollbackComplete function [Files]","fs.rollbackcomplete","ktmw32/RollbackComplete"]
old-location: fs\rollbackcomplete.htm
tech.root: fs
ms.assetid: c9d53777-eef9-4c60-921d-50b0fbf8d005
ms.date: 12/05/2018
ms.keywords: RollbackComplete, RollbackComplete function [Files], fs.rollbackcomplete, ktmw32/RollbackComplete
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
 - RollbackComplete
 - ktmw32/RollbackComplete
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
 - RollbackComplete
---

# RollbackComplete function


## -description

Indicates that the resource manager (RM) has successfully completed rolling back a transaction.

## -parameters

### -param EnlistmentHandle [in]

A handle the enlistment.

### -param TmVirtualClock [in]

The latest virtual clock value received for this transaction. See <a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a>.

## -returns

If the function succeeds, the return value is nonzero. 


  

If the function fails, the return value is zero (0). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

 The following list identifies the possible error codes:

## -remarks

If the RM was not able to successfully roll back a transaction, the RM should request a full rollback by calling the <a href="/windows/desktop/api/ktmw32/nf-ktmw32-rollbacktransaction">RollbackTransaction</a> function.

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-getcurrentclocktransactionmanager">GetCurrentClockTransactionManager</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>