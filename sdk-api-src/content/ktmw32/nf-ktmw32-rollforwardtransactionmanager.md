---
UID: NF:ktmw32.RollforwardTransactionManager
title: RollforwardTransactionManager function (ktmw32.h)
author: windows-sdk-content
description: Recovers information only to the specified virtual clock value.
old-location: fs\rollforwardtransactionmanager.htm
tech.root: ktm
ms.assetid: 13492b74-8707-46bb-93f1-59c3c5ceab6d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RollforwardTransactionManager, RollforwardTransactionManager function [Files], fs.rollforwardtransactionmanager, ktmw32/RollforwardTransactionManager
ms.topic: function
req.header: ktmw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - KtmW32.dll
api_name:
 - RollforwardTransactionManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RollforwardTransactionManager function


## -description


Recovers information only to the specified virtual clock value.


## -parameters




### -param TransactionManagerHandle [in]

A handle to the transaction manager.


### -param TmVirtualClock [in]

A pointer to the latest virtual clock value received for this transaction.


## -returns



If the function succeeds, the return value is nonzero.
      

If the function fails, the return value is 0 (zero). To get extended error information, call the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

The following list identifies the possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/21d7c0fa-3a49-43b3-9325-d3dfdabbcb98">GetCurrentClockTransactionManager</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>
 

 

