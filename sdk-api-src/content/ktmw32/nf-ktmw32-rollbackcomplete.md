---
UID: NF:ktmw32.RollbackComplete
title: RollbackComplete function
author: windows-sdk-content
description: Indicates that the resource manager (RM) has successfully completed rolling back a transaction.
old-location: fs\rollbackcomplete.htm
tech.root: Ktm
ms.assetid: c9d53777-eef9-4c60-921d-50b0fbf8d005
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: RollbackComplete, RollbackComplete function [Files], fs.rollbackcomplete, ktmw32/RollbackComplete
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
 - RollbackComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RollbackComplete function


## -description


Indicates that the resource manager (RM) has successfully completed rolling back a transaction.


## -parameters




### -param EnlistmentHandle [in]

A handle the enlistment.


### -param TmVirtualClock [in]

The latest virtual clock value received for this transaction. See <a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>.


## -returns



If the function succeeds, the return value is nonzero. 


  

If the function fails, the return value is zero (0). To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

 The following list identifies the possible error codes:




## -remarks



If the RM was not able to successfully roll back a transaction, the RM should request a full rollback by calling the <a href="https://msdn.microsoft.com/7d3522b8-ddf0-449e-8ab4-09e679ba1f15">RollbackTransaction</a> function.




## -see-also




<a href="https://msdn.microsoft.com/21d7c0fa-3a49-43b3-9325-d3dfdabbcb98">GetCurrentClockTransactionManager</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>
 

 

