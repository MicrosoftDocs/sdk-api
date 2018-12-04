---
UID: NF:ktmw32.CommitTransaction
title: CommitTransaction function
author: windows-sdk-content
description: Requests that the specified transaction be committed.
old-location: fs\committransaction.htm
tech.root: ktm
ms.assetid: 17db5e1f-685b-46f0-bac6-dff4c18bb515
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CommitTransaction, CommitTransaction function [Files], fs.committransaction, ktmw32/CommitTransaction
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - CommitTransaction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CommitTransaction function


## -description


Requests that the specified transaction be committed.


## -parameters




### -param TransactionHandle [in]

A handle to the transaction to be committed. 

This handle must have been opened with the TRANSACTION_COMMIT access right. For more information, see <a href="https://msdn.microsoft.com/c9d51d4d-9f07-44d6-a2e1-4a47367cc4ae">KTM Security and Access Rights</a>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

The following list identifies the possible error codes:




## -remarks



You can commit any transaction handle that has been opened or created using the TRANSACTION_COMMIT permission; any application can commit a transaction, not just the creator.

This function can only be called if the transaction is still active, not prepared, pre-prepared, or rolled back.




## -see-also




<a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>



<a href="https://msdn.microsoft.com/d95f15e4-d0fd-4665-849d-eecac8fc542b">OpenTransaction</a>



<a href="https://msdn.microsoft.com/7d3522b8-ddf0-449e-8ab4-09e679ba1f15">RollbackTransaction</a>
 

 

