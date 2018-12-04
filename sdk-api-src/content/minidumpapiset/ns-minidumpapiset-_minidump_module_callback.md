---
UID: NS:minidumpapiset._MINIDUMP_MODULE_CALLBACK
title: "_MINIDUMP_MODULE_CALLBACK"
author: windows-sdk-content
description: Contains module information for the MiniDumpCallback function when the callback type is ModuleCallback.
old-location: base\minidump_module_callback_str.htm
tech.root: debug
ms.assetid: 8ca48df0-ed0e-4ee3-a20a-d89057be37f3
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*PMINIDUMP_MODULE_CALLBACK, MINIDUMP_MODULE_CALLBACK, MINIDUMP_MODULE_CALLBACK structure, PMINIDUMP_MODULE_CALLBACK, PMINIDUMP_MODULE_CALLBACK structure pointer, _MINIDUMP_MODULE_CALLBACK, _win32_minidump_module_callback_str, base.minidump_module_callback_str, minidumpapiset/MINIDUMP_MODULE_CALLBACK, minidumpapiset/PMINIDUMP_MODULE_CALLBACK"
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
 - MINIDUMP_MODULE_CALLBACK
product: Windows
targetos: Windows
req.typenames: MINIDUMP_MODULE_CALLBACK, *PMINIDUMP_MODULE_CALLBACK
req.redist: DbgHelp.dll 5.1 or later
---

# _MINIDUMP_MODULE_CALLBACK structure


## -description


Contains module information for the 
<a href="https://msdn.microsoft.com/8dc95b0a-6aee-4c38-ab25-a800153bbe91">MiniDumpCallback</a> function when the callback type is 
<a href="https://msdn.microsoft.com/c970564d-e1f0-4317-bf66-752b98767451">ModuleCallback</a>.


## -struct-fields




### -field FullPath

The fully qualified path of the module executable.


### -field BaseOfImage

The base address of the module executable image in memory.


### -field SizeOfImage

The size of the module executable image in memory, in bytes.


### -field CheckSum

The checksum value of the module executable image.


### -field TimeDateStamp

The timestamp value of the module executable image, in <b>time_t</b> format.


### -field VersionInfo

A 
<a href="_win32_vs_fixedfileinfo_str">VS_FIXEDFILEINFO</a> structure that specifies the version of the module.


### -field CvRecord

A pointer to a string containing the CodeView record of the module.


### -field SizeOfCvRecord

The size of the Codeview record of the module in the <b>CvRecord</b> member, in bytes.


### -field MiscRecord

A pointer to a string that specifies the miscellaneous record of the module.


### -field SizeOfMiscRecord

The size of the miscellaneous record of the module in the <b>MiscRecord</b> member, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/0ce3083c-21c9-48a4-9099-1dab31afcafa">MINIDUMP_CALLBACK_INPUT</a>



<a href="https://msdn.microsoft.com/8dc95b0a-6aee-4c38-ab25-a800153bbe91">MiniDumpCallback</a>



<a href="_win32_vs_fixedfileinfo_str">VS_FIXEDFILEINFO</a>
 

 

