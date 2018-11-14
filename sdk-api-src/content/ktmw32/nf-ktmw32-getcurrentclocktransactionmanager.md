---
UID: NF:ktmw32.GetCurrentClockTransactionManager
title: GetCurrentClockTransactionManager function
author: windows-sdk-content
description: Obtains a virtual clock value from a transaction manager.
old-location: fs\getcurrentclocktransactionmanager_func.htm
tech.root: Ktm
ms.assetid: 21d7c0fa-3a49-43b3-9325-d3dfdabbcb98
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetCurrentClockTransactionManager, GetCurrentClockTransactionManager function [Files], fs.getcurrentclocktransactionmanager_func, ktmw32/GetCurrentClockTransactionManager
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
 - GetCurrentClockTransactionManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetCurrentClockTransactionManager
: 
---

# GetCurrentClockTransactionManager function


## -description


Obtains a virtual clock value from a transaction manager.


## -parameters




### -param TransactionManagerHandle [in]

A handle to the transaction manager to obtain a virtual clock value for.


### -param TmVirtualClock [out]

The latest virtual clock value for the transaction manager. See <a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.


The following list identifies the possible error codes:






## -see-also




<a href="https://msdn.microsoft.com/de3e3a26-3e56-4732-8e7c-945b45593aed">CommitComplete</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>



<a href="https://msdn.microsoft.com/47488c70-3409-4544-bcca-3415f91e7194">PrepareComplete</a>



<a href="https://msdn.microsoft.com/b4a70a51-2c49-4626-9fca-9ca6e0d21a53">PreprepareComplete</a>



<a href="https://msdn.microsoft.com/a6411fad-8ad0-4a31-9e09-0c18dd384634">ReadOnlyEnlistment</a>



<a href="https://msdn.microsoft.com/c9d53777-eef9-4c60-921d-50b0fbf8d005">RollbackComplete</a>



<a href="https://msdn.microsoft.com/e62c0c81-6802-4a76-94bb-617933490e83">RollbackEnlistment</a>



<a href="https://msdn.microsoft.com/8cc77686-e130-4b82-b2f5-70121b40e052">SinglePhaseReject</a>
 

 

