---
UID: NS:minwinbase._UNLOAD_DLL_DEBUG_INFO
title: "_UNLOAD_DLL_DEBUG_INFO"
author: windows-sdk-content
description: Contains information about a dynamic-link library (DLL) that has just been unloaded.
old-location: base\unload_dll_debug_info_str.htm
tech.root: Debug
ms.assetid: a4ece775-a49e-406b-8eae-264f978eb597
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*LPUNLOAD_DLL_DEBUG_INFO, LPUNLOAD_DLL_DEBUG_INFO, LPUNLOAD_DLL_DEBUG_INFO structure pointer, UNLOAD_DLL_DEBUG_INFO, UNLOAD_DLL_DEBUG_INFO structure, _UNLOAD_DLL_DEBUG_INFO, _win32_unload_dll_debug_info_str, base.unload_dll_debug_info_str, minwinbase/LPUNLOAD_DLL_DEBUG_INFO, minwinbase/UNLOAD_DLL_DEBUG_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: minwinbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minwinbase.h
api_name:
 - UNLOAD_DLL_DEBUG_INFO
product: Windows
targetos: Windows
req.typenames: UNLOAD_DLL_DEBUG_INFO, *LPUNLOAD_DLL_DEBUG_INFO
req.redist: 
---

# _UNLOAD_DLL_DEBUG_INFO structure


## -description


Contains information about a dynamic-link library (DLL) that has just been unloaded.


## -struct-fields




### -field lpBaseOfDll

A pointer to the base address of the DLL in the address space of the process unloading the DLL.


## -see-also




<a href="https://msdn.microsoft.com/056aa7ee-51ca-48ec-9cd7-26085bb85b11">DEBUG_EVENT</a>
 

 

