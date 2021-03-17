---
UID: NF:ktmw32.CommitComplete
title: CommitComplete function (ktmw32.h)
description: Indicates that a resource manager (RM) has finished committing a transaction that was requested by the transaction manager (TM).
helpviewer_keywords: ["CommitComplete","CommitComplete function [Files]","fs.commitcomplete","ktmw32/CommitComplete"]
old-location: fs\commitcomplete.htm
tech.root: fs
ms.assetid: de3e3a26-3e56-4732-8e7c-945b45593aed
ms.date: 12/05/2018
ms.keywords: CommitComplete, CommitComplete function [Files], fs.commitcomplete, ktmw32/CommitComplete
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
 - CommitComplete
 - ktmw32/CommitComplete
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
 - CommitComplete
---

# CommitComplete function


## -description

Indicates that a resource manager (RM) has finished committing a transaction that was requested by the transaction manager (TM).

## -parameters

### -param EnlistmentHandle [in]

A handle to the enlistment for which the commit operation is completed.

### -param TmVirtualClock [in]

The latest virtual clock value received for this transaction. If you specify <b>NULL</b>, the virtual clock value is not changed. See <a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a>.

To change the virtual clock value, this value must be greater than the current value returned in the COMMIT notification.

## -returns

If the function succeeds, the return value is nonzero. 


  

If the function fails, the return value is zero (0). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

 The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-createenlistment">CreateEnlistment</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-getcurrentclocktransactionmanager">GetCurrentClockTransactionManager</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>