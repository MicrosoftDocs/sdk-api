---
UID: NF:ktmw32.OpenTransactionManager
title: OpenTransactionManager function (ktmw32.h)
description: Opens an existing transaction manager. (OpenTransactionManager)
helpviewer_keywords: ["OpenTransactionManager","OpenTransactionManager function [Files]","fs.opentransactionmanager","ktmw32/OpenTransactionManager"]
old-location: fs\opentransactionmanager.htm
tech.root: fs
ms.assetid: 6b53609a-b956-441c-b5b5-9a8e6aa489c9
ms.date: 12/05/2018
ms.keywords: OpenTransactionManager, OpenTransactionManager function [Files], fs.opentransactionmanager, ktmw32/OpenTransactionManager
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
 - OpenTransactionManager
 - ktmw32/OpenTransactionManager
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
 - OpenTransactionManager
---

# OpenTransactionManager function


## -description

Opens an existing transaction manager.

## -parameters

### -param LogFileName [in]

The name of the log stream.  This stream must exist within a CLFS log file.

### -param DesiredAccess [in]

The access requested. See <a href="/windows/desktop/Ktm/transaction-manager-access-masks">Transaction Manager Access Masks</a> for a list of valid values.

### -param OpenOptions [in, optional]

Reserved; specify zero.

## -returns

If the function succeeds, the return value is a handle to the transaction manager.

If the function fails, the return value is INVALID_HANDLE_VALUE. To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

The following list identifies the  possible error codes:

## -remarks

Immediately after calling this function, you must call <a href="/windows/desktop/api/ktmw32/nf-ktmw32-recovertransactionmanager">RecoverTransactionManager</a>.

The <i>LogFileName</i> must be specified using the NT file format. For example: <i>\??\&lt;drive&gt;:\&lt;path&gt;</i>. Do not use the .BLF extension.

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransactionmanager">CreateTransactionManager</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-getcurrentclocktransactionmanager">GetCurrentClockTransactionManager</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-opentransactionmanagerbyid">OpenTransactionManagerById</a>



<a href="/windows/desktop/Ktm/transaction-manager-access-masks">Transaction Manager Access Masks</a>
