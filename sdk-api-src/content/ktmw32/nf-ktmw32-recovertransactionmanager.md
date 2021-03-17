---
UID: NF:ktmw32.RecoverTransactionManager
title: RecoverTransactionManager function (ktmw32.h)
description: Recovers a transaction manager's state from its log file.
helpviewer_keywords: ["RecoverTransactionManager","RecoverTransactionManager function [Files]","fs.recovertransactionmanager","ktmw32/RecoverTransactionManager"]
old-location: fs\recovertransactionmanager.htm
tech.root: fs
ms.assetid: 6f217ebb-3423-41d3-acff-eb21838c9751
ms.date: 12/05/2018
ms.keywords: RecoverTransactionManager, RecoverTransactionManager function [Files], fs.recovertransactionmanager, ktmw32/RecoverTransactionManager
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
 - RecoverTransactionManager
 - ktmw32/RecoverTransactionManager
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
 - RecoverTransactionManager
---

# RecoverTransactionManager function


## -description

Recovers a transaction manager's state from  its log file.

## -parameters

### -param TransactionManagerHandle [in]

A handle to the transaction manager.

## -returns

If the function succeeds, the return value is nonzero. 


  

If the function fails, the return value is zero (0). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

 The following list identifies the possible error codes:

## -remarks

This function must be called after you call <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransactionmanager">CreateTransactionManager</a>.

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransactionmanager">CreateTransactionManager</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>