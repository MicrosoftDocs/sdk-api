---
UID: NF:aux_ulib.AuxUlibInitialize
title: AuxUlibInitialize function (aux_ulib.h)
author: windows-sdk-content
description: Initializes the Aux_ulib library.
old-location: winprog\auxulibinitialize_func.htm
tech.root: DevNotes
ms.assetid: 2e46e323-669c-4fcd-b3e0-d1e4ec700c64
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AuxUlibInitialize, AuxUlibInitialize function [Windows API], aux_ulib/AuxUlibInitialize, winprog.auxulibinitialize_func
ms.topic: function
req.header: aux_ulib.h
req.include-header: 
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
req.lib: Aux_ulib.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Aux_ulib.lib
api_name:
 - AuxUlibInitialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Auxiliary API library version 1.0 or later
---

# AuxUlibInitialize function


## -description


Initializes the Aux_ulib library. This function must be called before any
    other function in the library can be called.


## -parameters






## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a6ee33e-91dc-4f6d-bdb7-a93b7478b58e">AuxUlibSetSystemFileCacheSize</a>
 

 

