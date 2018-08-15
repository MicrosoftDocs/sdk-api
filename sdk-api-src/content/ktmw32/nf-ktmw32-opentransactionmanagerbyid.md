---
UID: NF:ktmw32.OpenTransactionManagerById
title: OpenTransactionManagerById function
author: windows-sdk-content
description: Opens an existing transaction manager.
old-location: fs\opentransactionmanagerbyid.htm
old-project: ktm
ms.assetid: 4724383d-8ecf-40cb-8159-15a6d5ddfd1b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: OpenTransactionManagerById, OpenTransactionManagerById function [Files], fs.opentransactionmanagerbyid, ktmw32/OpenTransactionManagerById
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ktmw32.h
req.include-header: 
req.redist: 
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
 - OpenTransactionManagerById
product: Windows
targetos: Windows
req.lib: Ktmw32.lib
req.dll: Ktmw32.dll
req.irql: 
req.product: GDI+ 1.1
---

# OpenTransactionManagerById function


## -description


Opens an existing transaction manager.


## -parameters




### -param TransactionManagerId [in]

The identifier of the transaction to open.


### -param DesiredAccess [in]

The access requested. See <a href="https://msdn.microsoft.com/8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0">Transaction Manager Access Masks</a> for a list of valid values.


### -param OPTIONAL

TBD




#### - OpenOptions [in, optional]

Reserved; specify zero.


## -returns



If the function succeeds, the return value is a handle to the transaction manager.

If the function fails, the return value is INVALID_HANDLE_VALUE. To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

The following list identifies the  possible error codes:




## -remarks



Immediately after calling this function, you must call <a href="https://msdn.microsoft.com/6f217ebb-3423-41d3-acff-eb21838c9751">RecoverTransactionManager</a>.




## -see-also




<a href="https://msdn.microsoft.com/f5b7d0c1-9cd0-48fc-8125-d4da040951c4">CreateTransactionManager</a>



<a href="https://msdn.microsoft.com/21d7c0fa-3a49-43b3-9325-d3dfdabbcb98">GetCurrentClockTransactionManager</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>



<a href="https://msdn.microsoft.com/6b53609a-b956-441c-b5b5-9a8e6aa489c9">OpenTransactionManager</a>



<a href="https://msdn.microsoft.com/8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0">Transaction Manager Access Masks</a>
 

 

