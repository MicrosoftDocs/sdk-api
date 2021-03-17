---
UID: NS:minidumpapiset._MINIDUMP_MODULE_LIST
title: MINIDUMP_MODULE_LIST (minidumpapiset.h)
description: Contains a list of modules.
helpviewer_keywords: ["*PMINIDUMP_MODULE_LIST","MINIDUMP_MODULE_LIST","MINIDUMP_MODULE_LIST structure","PMINIDUMP_MODULE_LIST","PMINIDUMP_MODULE_LIST structure pointer","_MINIDUMP_MODULE_LIST","_win32_minidump_module_list_str","base.minidump_module_list_str","minidumpapiset/MINIDUMP_MODULE_LIST","minidumpapiset/PMINIDUMP_MODULE_LIST"]
old-location: base\minidump_module_list_str.htm
tech.root: Debug
ms.assetid: 9c30026d-9c72-472f-9d71-b15274459aae
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_MODULE_LIST, MINIDUMP_MODULE_LIST, MINIDUMP_MODULE_LIST structure, PMINIDUMP_MODULE_LIST, PMINIDUMP_MODULE_LIST structure pointer, _MINIDUMP_MODULE_LIST, _win32_minidump_module_list_str, base.minidump_module_list_str, minidumpapiset/MINIDUMP_MODULE_LIST, minidumpapiset/PMINIDUMP_MODULE_LIST'
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
req.typenames: MINIDUMP_MODULE_LIST, *PMINIDUMP_MODULE_LIST
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_MODULE_LIST
 - minidumpapiset/_MINIDUMP_MODULE_LIST
 - PMINIDUMP_MODULE_LIST
 - minidumpapiset/PMINIDUMP_MODULE_LIST
 - MINIDUMP_MODULE_LIST
 - minidumpapiset/MINIDUMP_MODULE_LIST
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
 - MINIDUMP_MODULE_LIST
---

# MINIDUMP_MODULE_LIST structure


## -description

Contains a list of modules.

## -struct-fields

### -field NumberOfModules

The number of structures in the <b>Modules</b> array.

### -field Modules

An array of 
<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_module">MINIDUMP_MODULE</a> structures.

## -see-also

<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_module">MINIDUMP_MODULE</a>



<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>