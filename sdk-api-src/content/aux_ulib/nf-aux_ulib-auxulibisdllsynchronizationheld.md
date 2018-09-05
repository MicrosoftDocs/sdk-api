---
UID: NF:aux_ulib.AuxUlibIsDLLSynchronizationHeld
title: AuxUlibIsDLLSynchronizationHeld function
author: windows-sdk-content
description: Determines whether the caller is holding a synchronization primitive.
old-location: winprog\auxulibisdllsynchronizationheld.htm
old-project: DevNotes
ms.assetid: fa2adb90-757c-4796-9842-e1f1a16d46fa
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AuxUlibIsDLLSynchronizationHeld, AuxUlibIsDLLSynchronizationHeld function [Windows API], aux_ulib/AuxUlibIsDLLSynchronizationHeld, winprog.auxulibisdllsynchronizationheld
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: aux_ulib.h
req.include-header: 
req.redist: Windows Auxiliary API library version 2.0
req.target-type: Windows
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
tech.root: 
req.typenames: AUTHZ_SOURCE_SCHEMA_REGISTRATION, *PAUTHZ_SOURCE_SCHEMA_REGISTRATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Aux_ulib.lib
api_name:
 - AuxUlibIsDLLSynchronizationHeld
product: Windows
targetos: Windows
req.lib: Aux_ulib.lib
req.dll: 
req.irql: 
---

# AuxUlibIsDLLSynchronizationHeld function


## -description


Determines whether the caller is holding a synchronization primitive. This information can be used to avoid operations that could potentially lead to deadlocks.


## -parameters




### -param SynchronizationHeld [out]

Indicates whether the caller is holding a synchronization primitive.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



You must call the <a href="https://msdn.microsoft.com/2e46e323-669c-4fcd-b3e0-d1e4ec700c64">AuxUlibInitialize</a> function before calling this function.

The object library that implements this API can be downloaded from <a href="Http://go.microsoft.com/fwlink/p/?linkid=85311">here</a>.



