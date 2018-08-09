---
UID: NF:ktmw32.RecoverTransactionManager
title: RecoverTransactionManager function
author: windows-sdk-content
description: Recovers a transaction manager's state from its log file.
old-location: fs\recovertransactionmanager.htm
old-project: ktm
ms.assetid: 6f217ebb-3423-41d3-acff-eb21838c9751
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RecoverTransactionManager, RecoverTransactionManager function [Files], fs.recovertransactionmanager, ktmw32/RecoverTransactionManager
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT, *PTRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ktmw32.dll
api_name:
 - RecoverTransactionManager
product: Windows
targetos: Windows
req.lib: Ktmw32.lib
req.dll: Ktmw32.dll
req.irql: 
req.product: GDI+ 1.1
---

# RecoverTransactionManager function


## -description


Recovers a transaction manager's state from  its log file.


## -parameters




### -param TransactionManagerHandle [in]

A handle to the transaction manager.


## -returns



If the function succeeds, the return value is nonzero. 


  

If the function fails, the return value is zero (0). To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

 The following list identifies the possible error codes:




## -remarks



This function must be called after you call <a href="https://msdn.microsoft.com/f5b7d0c1-9cd0-48fc-8125-d4da040951c4">CreateTransactionManager</a>.




## -see-also




<a href="https://msdn.microsoft.com/f5b7d0c1-9cd0-48fc-8125-d4da040951c4">CreateTransactionManager</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>
 

 

