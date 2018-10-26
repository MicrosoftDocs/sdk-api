---
UID: NF:aux_ulib.AuxUlibSetSystemFileCacheSize
title: AuxUlibSetSystemFileCacheSize function
author: windows-sdk-content
description: Sets the current file system cache size.
old-location: winprog\auxulibsetsystemfilecachesize_func.htm
tech.root: devnotes
ms.assetid: 2a6ee33e-91dc-4f6d-bdb7-a93b7478b58e
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: AuxUlibSetSystemFileCacheSize, AuxUlibSetSystemFileCacheSize function [Windows API], aux_ulib/AuxUlibSetSystemFileCacheSize, winprog.auxulibsetsystemfilecachesize_func
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - AuxUlibSetSystemFileCacheSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Auxiliary API library version 1.0 or later
---

# AuxUlibSetSystemFileCacheSize function


## -description


Sets the current file system cache size.

As of Windows Server 2003 with Service Pack 1 (SP1), this function has been superseded by the <a href="https://msdn.microsoft.com/bb0a65d6-d04a-4805-80d5-61fc53eb2726">SetSystemFileCacheSize</a> function.


## -parameters




### -param MinimumFileCacheSize [in]

The minimum cache size, in bytes. To flush the cache, use (<b>DWORD</b>)–1.


### -param MaximumFileCacheSize [in]

The maximum cache size, in bytes. To flush the cache, use (<b>DWORD</b>)–1.


### -param Flags [in]

This parameter is reserved for future use and must be zero.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



You must call the <a href="https://msdn.microsoft.com/2e46e323-669c-4fcd-b3e0-d1e4ec700c64">AuxUlibInitialize</a> function before calling this function.

The caller must have enabled the SE_INCREASE_QUOTA_NAME privilege in the active token.

The object library that implements this API can be downloaded from <a href="Http://go.microsoft.com/fwlink/p/?linkid=85311">here</a>.




## -see-also




<a href="https://msdn.microsoft.com/2e46e323-669c-4fcd-b3e0-d1e4ec700c64">AuxUlibInitialize</a>
 

 

