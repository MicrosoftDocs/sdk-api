---
UID: NS:minidumpapiset._MINIDUMP_INCLUDE_MODULE_CALLBACK
title: "_MINIDUMP_INCLUDE_MODULE_CALLBACK"
author: windows-sdk-content
description: Contains information for the MiniDumpCallback function when the callback type is IncludeModuleCallback.
old-location: base\minidump_include_module_callback_str.htm
tech.root: debug
ms.assetid: 01dd2217-fd7b-4bcf-a15e-4769c7518741
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*PMINIDUMP_INCLUDE_MODULE_CALLBACK, MINIDUMP_INCLUDE_MODULE_CALLBACK, MINIDUMP_INCLUDE_MODULE_CALLBACK structure, PMINIDUMP_INCLUDE_MODULE_CALLBACK, PMINIDUMP_INCLUDE_MODULE_CALLBACK structure pointer, _MINIDUMP_INCLUDE_MODULE_CALLBACK, _win32_minidump_include_module_callback_str, base.minidump_include_module_callback_str, minidumpapiset/MINIDUMP_INCLUDE_MODULE_CALLBACK, minidumpapiset/PMINIDUMP_INCLUDE_MODULE_CALLBACK"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_INCLUDE_MODULE_CALLBACK
product: Windows
targetos: Windows
req.typenames: MINIDUMP_INCLUDE_MODULE_CALLBACK, *PMINIDUMP_INCLUDE_MODULE_CALLBACK
req.redist: DbgHelp.dll 5.1 or later
---

# _MINIDUMP_INCLUDE_MODULE_CALLBACK structure


## -description


Contains information for the 
<a href="https://msdn.microsoft.com/8dc95b0a-6aee-4c38-ab25-a800153bbe91">MiniDumpCallback</a> function when the callback type is 
<b>IncludeModuleCallback</b>.


## -struct-fields




### -field BaseOfImage

The base address of the executable image in memory.


## -see-also




<a href="https://msdn.microsoft.com/0ce3083c-21c9-48a4-9099-1dab31afcafa">MINIDUMP_CALLBACK_INPUT</a>



<a href="https://msdn.microsoft.com/c970564d-e1f0-4317-bf66-752b98767451">MINIDUMP_CALLBACK_TYPE</a>



<a href="https://msdn.microsoft.com/8dc95b0a-6aee-4c38-ab25-a800153bbe91">MiniDumpCallback</a>
 

 

