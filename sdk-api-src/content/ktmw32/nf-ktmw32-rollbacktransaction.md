---
UID: NF:ktmw32.RollbackTransaction
title: RollbackTransaction function (ktmw32.h)
author: windows-sdk-content
description: Requests that the specified transaction be rolled back.
old-location: fs\rollbacktransaction.htm
tech.root: ktm
ms.assetid: 7d3522b8-ddf0-449e-8ab4-09e679ba1f15
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RollbackTransaction, RollbackTransaction function [Files], fs.rollbacktransaction, ktmw32/RollbackTransaction
ms.topic: function
f1_keywords: 
 - "ktmw32/RollbackTransaction"
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
 - RollbackTransaction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RollbackTransaction function


## -description



        Requests that the specified transaction be rolled back.  This function is synchronous.


## -parameters




### -param TransactionHandle [in]

A handle to the transaction.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. The following list identifies the possible error codes: 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-committransaction">CommitTransaction</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a>



<a href="https://docs.microsoft.com/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-opentransaction">OpenTransaction</a>
 

 

