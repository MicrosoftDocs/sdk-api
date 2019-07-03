---
UID: NS:minidumpapiset._MINIDUMP_MODULE_CALLBACK
title: MINIDUMP_MODULE_CALLBACK (minidumpapiset.h)
author: windows-sdk-content
description: Contains module information for the MiniDumpCallback function when the callback type is ModuleCallback.
old-location: base\minidump_module_callback_str.htm
tech.root: Debug
ms.assetid: 8ca48df0-ed0e-4ee3-a20a-d89057be37f3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PMINIDUMP_MODULE_CALLBACK, MINIDUMP_MODULE_CALLBACK, MINIDUMP_MODULE_CALLBACK structure, PMINIDUMP_MODULE_CALLBACK, PMINIDUMP_MODULE_CALLBACK structure pointer, _MINIDUMP_MODULE_CALLBACK, _win32_minidump_module_callback_str, base.minidump_module_callback_str, minidumpapiset/MINIDUMP_MODULE_CALLBACK, minidumpapiset/PMINIDUMP_MODULE_CALLBACK"
ms.topic: struct
f1_keywords: 
 - "minidumpapiset/MINIDUMP_MODULE_CALLBACK"
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
ms.custom: 19H1
---

# MINIDUMP_MODULE_CALLBACK structure


## -description


Contains module information for the 
<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a> function when the callback type is 
<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/ne-minidumpapiset-_minidump_callback_type">ModuleCallback</a>.


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
<a href="https://docs.microsoft.com/windows/desktop/api/verrsrc/ns-verrsrc-tagvs_fixedfileinfo">VS_FIXEDFILEINFO</a> structure that specifies the version of the module.


### -field CvRecord

A pointer to a string containing the CodeView record of the module.


### -field SizeOfCvRecord

The size of the Codeview record of the module in the <b>CvRecord</b> member, in bytes.


### -field MiscRecord

A pointer to a string that specifies the miscellaneous record of the module.


### -field SizeOfMiscRecord

The size of the miscellaneous record of the module in the <b>MiscRecord</b> member, in bytes.


## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_input">MINIDUMP_CALLBACK_INPUT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/verrsrc/ns-verrsrc-tagvs_fixedfileinfo">VS_FIXEDFILEINFO</a>
 

 

