---
UID: NS:minidumpapiset._MINIDUMP_MODULE
title: "_MINIDUMP_MODULE"
author: windows-driver-content
description: Contains information for a specific module.
old-location: base\minidump_module_str.htm
old-project: Debug
ms.assetid: 17e32c6e-29df-4308-b22d-39e13bc6a2a5
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: "*PMINIDUMP_MODULE, MINIDUMP_MODULE, MINIDUMP_MODULE structure, PMINIDUMP_MODULE, PMINIDUMP_MODULE structure pointer, _MINIDUMP_MODULE, _win32_minidump_module_str, base.minidump_module_str, minidumpapiset/MINIDUMP_MODULE, minidumpapiset/PMINIDUMP_MODULE"
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
req.typenames: MINIDUMP_MODULE, *PMINIDUMP_MODULE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	minidumpapiset.h
api_name:
-	MINIDUMP_MODULE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MINIDUMP_MODULE structure


## -description


Contains information for a specific module.


## -struct-fields




### -field BaseOfImage

The base address of the module executable image in memory.


### -field SizeOfImage

The size of the module executable image in memory, in bytes.


### -field CheckSum

The checksum value of the module executable image.


### -field TimeDateStamp

The timestamp value of the module executable image, in <b>time_t</b> format.


### -field ModuleNameRva

An RVA to a 
<a href="https://msdn.microsoft.com/b90b2b29-9d39-4a73-b5fb-bb6e04c94811">MINIDUMP_STRING</a> structure that specifies the name of the module.


### -field VersionInfo

A 
<a href="_win32_vs_fixedfileinfo_str">VS_FIXEDFILEINFO</a> structure that specifies the version of the module.


### -field CvRecord

 A <a href="https://msdn.microsoft.com/aef17239-9b56-4d49-8347-610270f8612b">MINIDUMP_LOCATION_DESCRIPTOR</a> structure that specifies the CodeView record of the module.


### -field MiscRecord

A <a href="https://msdn.microsoft.com/aef17239-9b56-4d49-8347-610270f8612b">MINIDUMP_LOCATION_DESCRIPTOR</a> structure that specifies the miscellaneous record of the module.


### -field Reserved0

Reserved for future use.


### -field Reserved1

Reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/9c30026d-9c72-472f-9d71-b15274459aae">MINIDUMP_MODULE_LIST</a>



<a href="https://msdn.microsoft.com/b90b2b29-9d39-4a73-b5fb-bb6e04c94811">MINIDUMP_STRING</a>



<a href="_win32_vs_fixedfileinfo_str">VS_FIXEDFILEINFO</a>
 

 

