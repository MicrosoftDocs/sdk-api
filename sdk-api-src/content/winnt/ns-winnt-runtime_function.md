---
UID: NS:winnt._IMAGE_RUNTIME_FUNCTION_ENTRY
title: RUNTIME_FUNCTION (winnt.h)
description: Represents an entry in the function table on 64-bit Windows.
helpviewer_keywords: ["*PRUNTIME_FUNCTION","*_PIMAGE_RUNTIME_FUNCTION_ENTRY","IMAGE_IA64_RUNTIME_FUNCTION_ENTRY","IMAGE_RUNTIME_FUNCTION_ENTRY","RUNTIME_FUNCTION","_IMAGE_RUNTIME_FUNCTION_ENTRY","_IMAGE_RUNTIME_FUNCTION_ENTRY structure","_PIMAGE_RUNTIME_FUNCTION_ENTRY","_PIMAGE_RUNTIME_FUNCTION_ENTRY structure pointer","base._image_runtime_function_entry","winnt/_IMAGE_RUNTIME_FUNCTION_ENTRY","winnt/_PIMAGE_RUNTIME_FUNCTION_ENTRY"]
old-location: base\_image_runtime_function_entry.htm
tech.root: Debug
ms.assetid: 9ed16f9a-3403-4ba9-9968-f51f6788a1f8
ms.date: 12/05/2018
ms.keywords: '*PRUNTIME_FUNCTION, *_PIMAGE_RUNTIME_FUNCTION_ENTRY, IMAGE_IA64_RUNTIME_FUNCTION_ENTRY, IMAGE_RUNTIME_FUNCTION_ENTRY, RUNTIME_FUNCTION, _IMAGE_RUNTIME_FUNCTION_ENTRY, _IMAGE_RUNTIME_FUNCTION_ENTRY structure, _PIMAGE_RUNTIME_FUNCTION_ENTRY, _PIMAGE_RUNTIME_FUNCTION_ENTRY structure pointer, base._image_runtime_function_entry, winnt/_IMAGE_RUNTIME_FUNCTION_ENTRY, winnt/_PIMAGE_RUNTIME_FUNCTION_ENTRY'
req.header: winnt.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RUNTIME_FUNCTION, *PRUNTIME_FUNCTION, _IMAGE_RUNTIME_FUNCTION_ENTRY, *_PIMAGE_RUNTIME_FUNCTION_ENTRY
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _IMAGE_RUNTIME_FUNCTION_ENTRY
 - winnt/_IMAGE_RUNTIME_FUNCTION_ENTRY
 - PRUNTIME_FUNCTION
 - winnt/PRUNTIME_FUNCTION
 - RUNTIME_FUNCTION
 - winnt/RUNTIME_FUNCTION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - _IMAGE_RUNTIME_FUNCTION_ENTRY
---

# RUNTIME_FUNCTION structure


## -description

Represents an entry in the function table on 64-bit Windows.

## -struct-fields

### -field BeginAddress

The address of the start of the function.

### -field EndAddress

The address of the end of the function.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.UnwindInfoAddress

The address of the unwind information for the function.

### -field DUMMYUNIONNAME.UnwindData

## -see-also

<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symfunctiontableaccess">SymFunctionTableAccess64</a>