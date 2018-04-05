---
UID: NF:ktmw32.GetEnlistmentId
title: GetEnlistmentId function
author: windows-driver-content
description: Obtains the identifier (ID) for the specified enlistment.
old-location: fs\getenlistmentid.htm
old-project: Ktm
ms.assetid: ffd37a2e-6bac-4566-bb15-eafce8a11c3b
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetEnlistmentId, GetEnlistmentId function [Files], fs.getenlistmentid, ktmw32/GetEnlistmentId
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
req.typenames: TRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT, *PTRANSACTION_NOTIFICATION_RECOVERY_ARGUMENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ktmw32.dll
api_name:
-	GetEnlistmentId
product: Windows
targetos: Windows
req.lib: Ktmw32.lib
req.dll: Ktmw32.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetEnlistmentId function


## -description


Obtains the identifier (ID) for the specified enlistment.


## -parameters




### -param EnlistmentHandle [in]

A handle to the enlistment.


### -param EnlistmentId [out]

A pointer to a variables that receives the ID of the enlistment.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.


The following list identifies the possible error codes:






## -see-also




<a href="https://msdn.microsoft.com/e9704ea8-e67d-4278-b77e-1d4787224d52">Kernel Transaction Manager Functions</a>
 

 

