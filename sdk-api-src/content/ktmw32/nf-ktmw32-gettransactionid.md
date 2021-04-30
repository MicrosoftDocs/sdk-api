---
UID: NF:ktmw32.GetTransactionId
title: GetTransactionId function (ktmw32.h)
description: Obtains the identifier (ID) for the specified transaction.
helpviewer_keywords: ["GetTransactionId","GetTransactionId function [Files]","fs.gettransactionid","ktmw32/GetTransactionId"]
old-location: fs\gettransactionid.htm
tech.root: fs
ms.assetid: 10f4729f-3e6e-469a-8f72-48c29735e7b1
ms.date: 12/05/2018
ms.keywords: GetTransactionId, GetTransactionId function [Files], fs.gettransactionid, ktmw32/GetTransactionId
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
 - GetTransactionId
 - ktmw32/GetTransactionId
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
 - GetTransactionId
---

# GetTransactionId function


## -description

Obtains the identifier (ID) for the specified transaction.

## -parameters

### -param TransactionHandle [in]

A handle to the transaction.

### -param TransactionId [out]

A pointer to a variable that receives the ID of the transaction.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.


The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>