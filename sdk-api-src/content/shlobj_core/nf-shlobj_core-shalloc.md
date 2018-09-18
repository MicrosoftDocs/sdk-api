---
UID: NF:shlobj_core.SHAlloc
title: SHAlloc function
author: windows-sdk-content
description: Allocates memory from the Shell's heap.
old-location: shell\SHAlloc.htm
tech.root: shell
ms.assetid: 621e4335-1484-4111-9cfe-7ae5c6d5c609
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: SHAlloc, SHAlloc function [Windows Shell], _win32_SHAlloc, shell.SHAlloc, shlobj_core/SHAlloc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHAlloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SHAlloc function


## -description


<p class="CCE_Message">[This function is available through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be altered or unavailable in subsequent versions of Windows. Use <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a> instead.]

Allocates memory from the Shell's heap.


## -parameters




### -param cb [in]

Type: <b>SIZE_T</b>

The number of bytes of memory to allocate.


## -returns



Type: <b>LPVOID</b>

A pointer to the allocated memory.




## -remarks



You can free this memory by calling <a href="https://msdn.microsoft.com/c9a532ad-ae24-4505-9e7b-577b90365441">SHFree</a>.



