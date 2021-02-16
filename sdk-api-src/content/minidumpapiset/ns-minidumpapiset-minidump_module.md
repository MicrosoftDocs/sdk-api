---
UID: NS:minidumpapiset._MINIDUMP_MODULE
title: MINIDUMP_MODULE (minidumpapiset.h)
description: Contains information for a specific module.
helpviewer_keywords: ["*PMINIDUMP_MODULE","MINIDUMP_MODULE","MINIDUMP_MODULE structure","PMINIDUMP_MODULE","PMINIDUMP_MODULE structure pointer","_MINIDUMP_MODULE","_win32_minidump_module_str","base.minidump_module_str","minidumpapiset/MINIDUMP_MODULE","minidumpapiset/PMINIDUMP_MODULE"]
old-location: base\minidump_module_str.htm
tech.root: Debug
ms.assetid: 17e32c6e-29df-4308-b22d-39e13bc6a2a5
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_MODULE, MINIDUMP_MODULE, MINIDUMP_MODULE structure, PMINIDUMP_MODULE, PMINIDUMP_MODULE structure pointer, _MINIDUMP_MODULE, _win32_minidump_module_str, base.minidump_module_str, minidumpapiset/MINIDUMP_MODULE, minidumpapiset/PMINIDUMP_MODULE'
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
targetos: Windows
req.typenames: MINIDUMP_MODULE, *PMINIDUMP_MODULE
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_MODULE
 - minidumpapiset/_MINIDUMP_MODULE
 - PMINIDUMP_MODULE
 - minidumpapiset/PMINIDUMP_MODULE
 - MINIDUMP_MODULE
 - minidumpapiset/MINIDUMP_MODULE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_MODULE
---

# MINIDUMP_MODULE structure


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
<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_string">MINIDUMP_STRING</a> structure that specifies the name of the module.

### -field VersionInfo

A 
<a href="/windows/desktop/api/verrsrc/ns-verrsrc-vs_fixedfileinfo">VS_FIXEDFILEINFO</a> structure that specifies the version of the module.

### -field CvRecord

 A <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_location_descriptor">MINIDUMP_LOCATION_DESCRIPTOR</a> structure that specifies the CodeView record of the module.

### -field MiscRecord

A <a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_location_descriptor">MINIDUMP_LOCATION_DESCRIPTOR</a> structure that specifies the miscellaneous record of the module.

### -field Reserved0

Reserved for future use.

### -field Reserved1

Reserved for future use.

## -see-also

<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_module_list">MINIDUMP_MODULE_LIST</a>



<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_string">MINIDUMP_STRING</a>



<a href="/windows/desktop/api/verrsrc/ns-verrsrc-vs_fixedfileinfo">VS_FIXEDFILEINFO</a>