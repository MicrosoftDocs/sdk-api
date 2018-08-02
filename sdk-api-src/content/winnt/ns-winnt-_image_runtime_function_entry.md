---
UID: NS:winnt._IMAGE_RUNTIME_FUNCTION_ENTRY
title: "_IMAGE_RUNTIME_FUNCTION_ENTRY"
author: windows-sdk-content
description: Represents an entry in the function table on 64-bit Windows.
old-location: base\_image_runtime_function_entry.htm
old-project: Debug
ms.assetid: 9ed16f9a-3403-4ba9-9968-f51f6788a1f8
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PRUNTIME_FUNCTION, *_PIMAGE_RUNTIME_FUNCTION_ENTRY, IMAGE_IA64_RUNTIME_FUNCTION_ENTRY, IMAGE_RUNTIME_FUNCTION_ENTRY, RUNTIME_FUNCTION, _IMAGE_RUNTIME_FUNCTION_ENTRY, _IMAGE_RUNTIME_FUNCTION_ENTRY structure, _PIMAGE_RUNTIME_FUNCTION_ENTRY, _PIMAGE_RUNTIME_FUNCTION_ENTRY structure pointer, base._image_runtime_function_entry, winnt/_IMAGE_RUNTIME_FUNCTION_ENTRY, winnt/_PIMAGE_RUNTIME_FUNCTION_ENTRY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: RUNTIME_FUNCTION, *PRUNTIME_FUNCTION, _IMAGE_RUNTIME_FUNCTION_ENTRY, *_PIMAGE_RUNTIME_FUNCTION_ENTRY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - _IMAGE_RUNTIME_FUNCTION_ENTRY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _IMAGE_RUNTIME_FUNCTION_ENTRY structure


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




<a href="https://msdn.microsoft.com/f79e6af9-9931-4bd7-ae12-29d890267a89">SymFunctionTableAccess64</a>
 

 

