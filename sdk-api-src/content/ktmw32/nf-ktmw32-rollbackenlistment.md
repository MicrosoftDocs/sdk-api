---
UID: NF:ktmw32.RollbackEnlistment
title: RollbackEnlistment function
author: windows-sdk-content
description: Rolls back the specified transaction that is associated with an enlistment. This function cannot be called for read-only enlistments.
old-location: fs\rollbackenlistment.htm
old-project: Ktm
ms.assetid: e62c0c81-6802-4a76-94bb-617933490e83
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: RollbackEnlistment, RollbackEnlistment function [Files], fs.rollbackenlistment, ktmw32/RollbackEnlistment
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
 - RollbackEnlistment
product: Windows
targetos: Windows
req.lib: Ktmw32.lib
req.dll: Ktmw32.dll
req.irql: 
req.product: GDI+ 1.1
---

# RollbackEnlistment function


## -description


Rolls back the specified transaction that is associated with an enlistment. This function cannot be called for read-only enlistments.


## -parameters




### -param EnlistmentHandle [in]

A handle to the enlistment.


### -param TmVirtualClock [in]

The latest virtual clock value received for this enlistment. See <a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>.


## -returns



If the function succeeds, the return value is nonzero. 


  

If the function fails, the return value is zero (0). To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

 The following list identifies the possible error codes:




## -remarks



This function is used by an RM to roll back a transaction in which it is enlisted. All work associated with the transaction is rolled back. 

Rollbacks are allowed by enlistments at any time before it issues a prepare complete notification.




## -see-also




<a href="https://msdn.microsoft.com/21d7c0fa-3a49-43b3-9325-d3dfdabbcb98">GetCurrentClockTransactionManager</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>



<a href="https://msdn.microsoft.com/a6411fad-8ad0-4a31-9e09-0c18dd384634">ReadOnlyEnlistment</a>
 

 

