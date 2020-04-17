---
UID: NF:ktmw32.OpenTransactionManagerById
title: OpenTransactionManagerById function (ktmw32.h)
description: Opens an existing transaction manager.helpviewer_keywords: ["OpenTransactionManagerById","OpenTransactionManagerById function [Files]","fs.opentransactionmanagerbyid","ktmw32/OpenTransactionManagerById"]
old-location: fs\opentransactionmanagerbyid.htm
tech.root: ktm
ms.assetid: 4724383d-8ecf-40cb-8159-15a6d5ddfd1b
ms.date: 12/05/2018
ms.keywords: OpenTransactionManagerById, OpenTransactionManagerById function [Files], fs.opentransactionmanagerbyid, ktmw32/OpenTransactionManagerById
f1_keywords:
- ktmw32/OpenTransactionManagerById
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ktmw32.dll
api_name:
- OpenTransactionManagerById
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OpenTransactionManagerById function


## -description


Opens an existing transaction manager.


## -parameters




### -param TransactionManagerId [in]

The identifier of the transaction to open.


### -param DesiredAccess [in]

The access requested. See <a href="https://docs.microsoft.com/windows/desktop/Ktm/transaction-manager-access-masks">Transaction Manager Access Masks</a> for a list of valid values.


### -param OpenOptions [in, optional]

Reserved; specify zero.


## -returns



If the function succeeds, the return value is a handle to the transaction manager.

If the function fails, the return value is INVALID_HANDLE_VALUE. To get extended error information, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

The following list identifies the  possible error codes:




## -remarks



Immediately after calling this function, you must call <a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-recovertransactionmanager">RecoverTransactionManager</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-createtransactionmanager">CreateTransactionManager</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-getcurrentclocktransactionmanager">GetCurrentClockTransactionManager</a>



<a href="https://docs.microsoft.com/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-opentransactionmanager">OpenTransactionManager</a>



<a href="https://docs.microsoft.com/windows/desktop/Ktm/transaction-manager-access-masks">Transaction Manager Access Masks</a>
 

 

