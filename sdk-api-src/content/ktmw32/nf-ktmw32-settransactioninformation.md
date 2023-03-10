---
UID: NF:ktmw32.SetTransactionInformation
title: SetTransactionInformation function (ktmw32.h)
description: Sets the transaction information for the specified transaction.
helpviewer_keywords: ["SetTransactionInformation","SetTransactionInformation function [Files]","fs.settransactioninformation","ktmw32/SetTransactionInformation"]
old-location: fs\settransactioninformation.htm
tech.root: fs
ms.assetid: e33d221b-cd06-4f20-a4b5-407a04362ba0
ms.date: 12/05/2018
ms.keywords: SetTransactionInformation, SetTransactionInformation function [Files], fs.settransactioninformation, ktmw32/SetTransactionInformation
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
 - SetTransactionInformation
 - ktmw32/SetTransactionInformation
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
 - SetTransactionInformation
---

# SetTransactionInformation function


## -description

Sets the transaction information for the specified transaction.

## -parameters

### -param TransactionHandle [in]

A handle to the transaction. The handle must have the TRANSACTION_SET_INFORMATION permission to set the transaction information.

### -param IsolationLevel [in, optional]

Reserved; specify zero.

### -param IsolationFlags [in, optional]

Reserved.

### -param Timeout [in, optional]

The timeout value, in milliseconds, for this transaction.

### -param Description [in, optional]

The user-defined description of this transaction.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.


The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-gettransactioninformation">GetTransactionInformation</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>