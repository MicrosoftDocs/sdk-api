---
UID: NF:ktmw32.GetTransactionInformation
title: GetTransactionInformation function (ktmw32.h)
description: Returns the requested information about the specified transaction.
helpviewer_keywords: ["GetTransactionInformation","GetTransactionInformation function [Files]","fs.gettransactioninformation_func","ktmw32/GetTransactionInformation"]
old-location: fs\gettransactioninformation_func.htm
tech.root: fs
ms.assetid: 5ce3c96a-629e-49d0-8ec4-f9bf76af99ac
ms.date: 12/05/2018
ms.keywords: GetTransactionInformation, GetTransactionInformation function [Files], fs.gettransactioninformation_func, ktmw32/GetTransactionInformation
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
 - GetTransactionInformation
 - ktmw32/GetTransactionInformation
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
 - GetTransactionInformation
---

# GetTransactionInformation function


## -description

Returns the requested information about the specified transaction.

## -parameters

### -param TransactionHandle [in]

A handle to the transaction. The handle must have  the TRANSACTION_QUERY_INFORMATION permission to retrieve the information.

### -param Outcome [out, optional]

A pointer to a buffer that receives the current outcome of the transaction. If the call to the <b>GetTransactionInformation</b> function is successful, this value will be one of the <a href="/windows/desktop/api/winnt/ne-winnt-transaction_outcome">TRANSACTION_OUTCOME</a> enumeration values.

### -param IsolationLevel [out, optional]

Reserved.

### -param IsolationFlags [out, optional]

Reserved.

### -param Timeout [out, optional]

A pointer to a variable that receives the timeout value, in milliseconds, for this transaction.

### -param BufferLength [in]

The size of the <i>Description</i> parameter, in bytes. The buffer length value cannot be longer than the value of MAX_TRANSACTION_DESCRIPTION_LENGTH.

### -param Description [out, optional]

A pointer to a buffer that receives the user-defined description of the transaction.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.


The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-settransactioninformation">SetTransactionInformation</a>