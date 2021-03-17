---
UID: NS:minwinbase._UNLOAD_DLL_DEBUG_INFO
title: UNLOAD_DLL_DEBUG_INFO (minwinbase.h)
description: Contains information about a dynamic-link library (DLL) that has just been unloaded.
helpviewer_keywords: ["*LPUNLOAD_DLL_DEBUG_INFO","LPUNLOAD_DLL_DEBUG_INFO","LPUNLOAD_DLL_DEBUG_INFO structure pointer","UNLOAD_DLL_DEBUG_INFO","UNLOAD_DLL_DEBUG_INFO structure","_UNLOAD_DLL_DEBUG_INFO","_win32_unload_dll_debug_info_str","base.unload_dll_debug_info_str","minwinbase/LPUNLOAD_DLL_DEBUG_INFO","minwinbase/UNLOAD_DLL_DEBUG_INFO"]
old-location: base\unload_dll_debug_info_str.htm
tech.root: Debug
ms.assetid: a4ece775-a49e-406b-8eae-264f978eb597
ms.date: 12/05/2018
ms.keywords: '*LPUNLOAD_DLL_DEBUG_INFO, LPUNLOAD_DLL_DEBUG_INFO, LPUNLOAD_DLL_DEBUG_INFO structure pointer, UNLOAD_DLL_DEBUG_INFO, UNLOAD_DLL_DEBUG_INFO structure, _UNLOAD_DLL_DEBUG_INFO, _win32_unload_dll_debug_info_str, base.unload_dll_debug_info_str, minwinbase/LPUNLOAD_DLL_DEBUG_INFO, minwinbase/UNLOAD_DLL_DEBUG_INFO'
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
targetos: Windows
req.typenames: UNLOAD_DLL_DEBUG_INFO, *LPUNLOAD_DLL_DEBUG_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _UNLOAD_DLL_DEBUG_INFO
 - minwinbase/_UNLOAD_DLL_DEBUG_INFO
 - LPUNLOAD_DLL_DEBUG_INFO
 - minwinbase/LPUNLOAD_DLL_DEBUG_INFO
 - UNLOAD_DLL_DEBUG_INFO
 - minwinbase/UNLOAD_DLL_DEBUG_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minwinbase.h
api_name:
 - UNLOAD_DLL_DEBUG_INFO
---

# UNLOAD_DLL_DEBUG_INFO structure


## -description

Contains information about a dynamic-link library (DLL) that has just been unloaded.

## -struct-fields

### -field lpBaseOfDll

A pointer to the base address of the DLL in the address space of the process unloading the DLL.

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-debug_event">DEBUG_EVENT</a>