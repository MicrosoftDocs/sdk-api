---
UID: NS:minidumpapiset._MINIDUMP_UNLOADED_MODULE
title: MINIDUMP_UNLOADED_MODULE (minidumpapiset.h)
description: Contains information about a module that has been unloaded. This information can help diagnose problems calling code that is no longer loaded.
helpviewer_keywords: ["*PMINIDUMP_UNLOADED_MODULE","MINIDUMP_UNLOADED_MODULE","MINIDUMP_UNLOADED_MODULE structure","PMINIDUMP_UNLOADED_MODULE","PMINIDUMP_UNLOADED_MODULE structure pointer","_MINIDUMP_UNLOADED_MODULE","_win32_minidump_unloaded_module_str","base.minidump_unloaded_module_str","minidumpapiset/MINIDUMP_UNLOADED_MODULE","minidumpapiset/PMINIDUMP_UNLOADED_MODULE"]
old-location: base\minidump_unloaded_module_str.htm
tech.root: Debug
ms.assetid: d2ae58fa-561c-4135-a757-88598ebda57a
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_UNLOADED_MODULE, MINIDUMP_UNLOADED_MODULE, MINIDUMP_UNLOADED_MODULE structure, PMINIDUMP_UNLOADED_MODULE, PMINIDUMP_UNLOADED_MODULE structure pointer, _MINIDUMP_UNLOADED_MODULE, _win32_minidump_unloaded_module_str, base.minidump_unloaded_module_str, minidumpapiset/MINIDUMP_UNLOADED_MODULE, minidumpapiset/PMINIDUMP_UNLOADED_MODULE'
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
req.typenames: MINIDUMP_UNLOADED_MODULE, *PMINIDUMP_UNLOADED_MODULE
req.redist: DbgHelp.dll 6.0 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_UNLOADED_MODULE
 - minidumpapiset/_MINIDUMP_UNLOADED_MODULE
 - PMINIDUMP_UNLOADED_MODULE
 - minidumpapiset/PMINIDUMP_UNLOADED_MODULE
 - MINIDUMP_UNLOADED_MODULE
 - minidumpapiset/MINIDUMP_UNLOADED_MODULE
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
 - MINIDUMP_UNLOADED_MODULE
---

# MINIDUMP_UNLOADED_MODULE structure


## -description

Contains information about a module that has been unloaded. This information can help diagnose problems calling code that is no longer loaded.

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

## -see-also

<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_unloaded_module_list">MINIDUMP_UNLOADED_MODULE_LIST</a>