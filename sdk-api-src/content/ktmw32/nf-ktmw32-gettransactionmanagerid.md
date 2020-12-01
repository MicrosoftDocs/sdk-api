---
UID: NF:ktmw32.GetTransactionManagerId
title: GetTransactionManagerId function (ktmw32.h)
description: Obtains an identifier for the specified transaction manager.
helpviewer_keywords: ["GetTransactionManagerId","GetTransactionManagerId function [Files]","fs.getidentitytransactionmanager_func","fs.gettransactionmanagerid","ktmw32/GetTransactionManagerId"]
old-location: fs\gettransactionmanagerid.htm
tech.root: fs
ms.assetid: e1aa573d-add9-42b7-8b2b-773dc12aa51b
ms.date: 12/05/2018
ms.keywords: GetTransactionManagerId, GetTransactionManagerId function [Files], fs.getidentitytransactionmanager_func, fs.gettransactionmanagerid, ktmw32/GetTransactionManagerId
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
 - GetTransactionManagerId
 - ktmw32/GetTransactionManagerId
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
 - GetTransactionManagerId
---

# GetTransactionManagerId function


## -description

Obtains an identifier for the specified transaction manager.

## -parameters

### -param TransactionManagerHandle [in]

A handle to the transaction manager.

### -param TransactionManagerId [out]

A pointer to a variable that receives the identifier for the transaction manager.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.


The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/api/ktmw32/nf-ktmw32-opentransactionmanager">OpenTransactionManager</a>