---
UID: NF:ktmw32.GetTransactionManagerId
title: GetTransactionManagerId function (ktmw32.h)
author: windows-sdk-content
description: Obtains an identifier for the specified transaction manager.
old-location: fs\gettransactionmanagerid.htm
tech.root: ktm
ms.assetid: e1aa573d-add9-42b7-8b2b-773dc12aa51b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTransactionManagerId, GetTransactionManagerId function [Files], fs.getidentitytransactionmanager_func, fs.gettransactionmanagerid, ktmw32/GetTransactionManagerId
ms.topic: function
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
 - GetTransactionManagerId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.


The following list identifies the possible error codes:






## -see-also




<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>



<a href="https://msdn.microsoft.com/6b53609a-b956-441c-b5b5-9a8e6aa489c9">OpenTransactionManager</a>
 

 

