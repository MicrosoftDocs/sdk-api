---
UID: NF:ktmw32.ReadOnlyEnlistment
title: ReadOnlyEnlistment function (ktmw32.h)
description: Requests that the specified enlistment be converted to a read-only enlistment. A read-only enlistment cannot participate in the outcome of the transaction and is not durably recorded for recovery.
helpviewer_keywords: ["ReadOnlyEnlistment","ReadOnlyEnlistment function [Files]","fs.readonlyenlistment","ktmw32/ReadOnlyEnlistment"]
old-location: fs\readonlyenlistment.htm
tech.root: fs
ms.assetid: a6411fad-8ad0-4a31-9e09-0c18dd384634
ms.date: 12/05/2018
ms.keywords: ReadOnlyEnlistment, ReadOnlyEnlistment function [Files], fs.readonlyenlistment, ktmw32/ReadOnlyEnlistment
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
 - ReadOnlyEnlistment
 - ktmw32/ReadOnlyEnlistment
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
 - ReadOnlyEnlistment
---

# ReadOnlyEnlistment function


## -description

Requests  that the specified enlistment be converted to a read-only enlistment. A read-only enlistment cannot participate in the outcome of the transaction  and is not durably recorded for recovery.

## -parameters

### -param EnlistmentHandle [in]

A handle to the enlistment.

### -param TmVirtualClock [in]

The latest virtual clock value received for this enlistment. If you specify <b>NULL</b>, the virtual clock value is not changed. See <a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a>.

To change the virtual clock value, this value must be greater than the current value returned in the COMMIT notification.

## -returns

If the function succeeds, the return value is nonzero. 


  

If the function fails, the return value is zero (0). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

 The following list identifies the possible error codes:

## -remarks

If a resource manager no longer needs to participate in a transaction without rolling  back the transaction, it should call  <b>ReadOnlyEnlistment</b> prior to closing the enlistment handle.

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-getcurrentclocktransactionmanager">GetCurrentClockTransactionManager</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-readonlyenlistment">ReadOnlyEnlistment</a>