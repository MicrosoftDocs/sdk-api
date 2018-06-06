---
UID: NF:ktmw32.SinglePhaseReject
title: SinglePhaseReject function
author: windows-sdk-content
description: Indicates that the resource manager (RM) is refusing a single-phase request. When a transaction manager (TM) receives this call, it initiates a two-phase commit and sends a prepare request to all enlisted RMs.
old-location: fs\singlephasereject.htm
old-project: Ktm
ms.assetid: 8cc77686-e130-4b82-b2f5-70121b40e052
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: SinglePhaseReject, SinglePhaseReject function [Files], fs.singlephasereject, ktmw32/SinglePhaseReject
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
 - SinglePhaseReject
product: Windows
targetos: Windows
req.lib: Ktmw32.lib
req.dll: Ktmw32.dll
req.irql: 
req.product: GDI+ 1.1
---

# SinglePhaseReject function


## -description


Indicates that the resource manager (RM) is refusing a single-phase request. When a transaction manager (TM) receives this call, it initiates a two-phase commit and sends a prepare request to all enlisted RMs.


## -parameters




### -param EnlistmentHandle [in]

A handle to the enlistment.


### -param TmVirtualClock [in]

The latest virtual clock value received from the single-phase request notification. If you specify <b>NULL</b>, the virtual clock value is not changed. See <a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a>.

To change the virtual clock value, this value must be greater than the current value returned in the COMMIT notification.


## -returns



If the function succeeds, the return value is nonzero. 


  

If the function fails, the return value is zero (0). To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

 The following list identifies the possible error codes:




## -see-also




<a href="https://msdn.microsoft.com/21d7c0fa-3a49-43b3-9325-d3dfdabbcb98">GetCurrentClockTransactionManager</a>



<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>
 

 

