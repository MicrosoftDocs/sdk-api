---
UID: NF:ktmw32.CreateTransactionManager
title: CreateTransactionManager function (ktmw32.h)
description: Creates a new transaction manager (TM) object and returns a handle with the specified access.
helpviewer_keywords: ["CreateTransactionManager","CreateTransactionManager function [Files]","TRANSACTION_MANAGER_VOLATILE","fs.createtransactionmanager","ktmw32/CreateTransactionManager"]
old-location: fs\createtransactionmanager.htm
tech.root: fs
ms.assetid: f5b7d0c1-9cd0-48fc-8125-d4da040951c4
ms.date: 12/05/2018
ms.keywords: CreateTransactionManager, CreateTransactionManager function [Files], TRANSACTION_MANAGER_VOLATILE, fs.createtransactionmanager, ktmw32/CreateTransactionManager
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
 - CreateTransactionManager
 - ktmw32/CreateTransactionManager
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
 - CreateTransactionManager
---

# CreateTransactionManager function


## -description

Creates a new transaction manager (TM) object and returns a handle with the specified access.

## -parameters

### -param lpTransactionAttributes [in, optional]

The transaction <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> (ACLs) for the TM object.

### -param LogFileName [in, optional]

The log file stream name.  If the stream does not exist in the log, it is created. To create a volatile TM, this parameter must be <b>NULL</b> and <i>CreateOptions</i> must specify TRANSACTION_MANAGER_VOLATILE, this transaction manager is considered volatile.

### -param CreateOptions [in, optional]

Any optional attributes for the new TM.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRANSACTION_MANAGER_VOLATILE"></a><a id="transaction_manager_volatile"></a><dl>
<dt><b>TRANSACTION_MANAGER_VOLATILE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the TM is volatile, and does not perform recovery.

</td>
</tr>
</table>

### -param CommitStrength [in, optional]

Reserved; specify zero.

## -returns

If the function succeeds, the return value is a handle to the transaction manager.  

If the function fails, the return value is INVALID_HANDLE_VALUE. To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

 The following list identifies the possible error codes:

## -remarks

Immediately after calling this function, you must call <a href="/windows/desktop/api/ktmw32/nf-ktmw32-recovertransactionmanager">RecoverTransactionManager</a>.

If your transaction manager is volatile, all your resource managers must also be volatile.

You must call <a href="/windows/desktop/api/ktmw32/nf-ktmw32-recovertransactionmanager">RecoverTransactionManager</a> after creating a TM in order for the TM to function correctly.

## -see-also

<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-opentransactionmanager">OpenTransactionManager</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-recovertransactionmanager">RecoverTransactionManager</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>