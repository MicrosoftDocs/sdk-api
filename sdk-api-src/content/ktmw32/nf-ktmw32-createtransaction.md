---
UID: NF:ktmw32.CreateTransaction
title: CreateTransaction function (ktmw32.h)
description: Creates a new transaction object.
helpviewer_keywords: ["CreateTransaction","CreateTransaction function [Files]","TRANSACTION_DO_NOT_PROMOTE","fs.createtransaction","ktmw32/CreateTransaction"]
old-location: fs\createtransaction.htm
tech.root: fs
ms.assetid: 578bda35-bd35-4f6d-8366-a4bfb4dbfe42
ms.date: 12/05/2018
ms.keywords: CreateTransaction, CreateTransaction function [Files], TRANSACTION_DO_NOT_PROMOTE, fs.createtransaction, ktmw32/CreateTransaction
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
req.lib: KtmW32.lib
req.dll: KtmW32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateTransaction
 - ktmw32/CreateTransaction
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
 - CreateTransaction
---

# CreateTransaction function


## -description

Creates a new transaction object.

## -parameters

### -param lpTransactionAttributes [in, optional]

A pointer to a <a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> 
      structure that determines whether the returned handle can be inherited by child processes. If this parameter is 
      <b>NULL</b>, the handle cannot be inherited.
      

The <b>lpSecurityDescriptor</b> member of the structure specifies a 
       <a href="/windows/desktop/winstation/desktop-security-and-access-rights">security descriptor</a> for the new 
       event. If <i>lpTransactionAttributes</i> is <b>NULL</b>, the object gets 
       a default security descriptor. The access control lists (ACL) in the default security descriptor for a 
       transaction come from the primary or impersonation token of the creator.

### -param UOW [in, optional]

Reserved. Must be zero (0).

### -param CreateOptions [in, optional]

Any optional transaction instructions.  

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRANSACTION_DO_NOT_PROMOTE"></a><a id="transaction_do_not_promote"></a><dl>
<dt><b>TRANSACTION_DO_NOT_PROMOTE</b></dt>
</dl>
</td>
<td width="60%">
The transaction cannot be distributed.

</td>
</tr>
</table>

### -param IsolationLevel [in, optional]

Reserved; specify zero (0).

### -param IsolationFlags [in, optional]

Reserved; specify zero (0).

### -param Timeout [in, optional]

The time-out interval, in milliseconds. If a nonzero value is specified, the transaction will be aborted when the interval elapses if it has not already reached the prepared state.

Specify zero (0) or INFINITE to provide an infinite time-out.

### -param Description [in, optional]

A user-readable description of the transaction.

## -returns

If the function succeeds, the return value is a handle to the transaction.
      

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended 
       error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

The following list identifies the possible error codes:

## -remarks

Use the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the transaction 
    handle. If the last transaction handle is closed before a client  calls the 
    <a href="/windows/desktop/api/ktmw32/nf-ktmw32-committransaction">CommitTransaction</a> function with the transaction 
    handle, then  KTM rolls back the transaction.

If the transaction might need to be promotable to a distributed transaction, then you must grant the Distributed Transaction Coordinator (DTC)  access rights to enlist in the transaction.  To do this, the  <i>lpTransactionAttributes</i> parameter needs to contain an access control entry with the DTC’s SID (S-1-5-80-2818357584-3387065753-4000393942-342927828-138088443) and the TRANSACTION_ENLIST right. For more information, see <a href="/previous-versions/windows/desktop/ms684146(v=vs.85)">Distributed Transaction Coordinator</a> and <a href="/windows/desktop/SecAuthZ/access-control-components">Access Control Components</a>.

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-committransaction">CommitTransaction</a>



<a href="/previous-versions/windows/desktop/ms684146(v=vs.85)">Distributed Transaction Coordinator</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-rollbacktransaction">RollbackTransaction</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-settransactioninformation">SetTransactionInformation</a>