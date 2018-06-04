---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

