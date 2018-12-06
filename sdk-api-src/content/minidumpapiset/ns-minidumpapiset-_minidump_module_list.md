---
UID: NS:minidumpapiset._MINIDUMP_MODULE_LIST
title: "_MINIDUMP_MODULE_LIST"
author: windows-sdk-content
description: Contains a list of modules.
old-location: base\minidump_module_list_str.htm
tech.root: debug
ms.assetid: 9c30026d-9c72-472f-9d71-b15274459aae
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PMINIDUMP_MODULE_LIST, MINIDUMP_MODULE_LIST, MINIDUMP_MODULE_LIST structure, PMINIDUMP_MODULE_LIST, PMINIDUMP_MODULE_LIST structure pointer, _MINIDUMP_MODULE_LIST, _win32_minidump_module_list_str, base.minidump_module_list_str, minidumpapiset/MINIDUMP_MODULE_LIST, minidumpapiset/PMINIDUMP_MODULE_LIST"
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
 - MINIDUMP_MODULE_LIST
product: Windows
targetos: Windows
req.typenames: MINIDUMP_MODULE_LIST, *PMINIDUMP_MODULE_LIST
req.redist: DbgHelp.dll 5.1 or later
---

# _MINIDUMP_MODULE_LIST structure


## -description


Contains a list of modules.


## -struct-fields




### -field NumberOfModules

The number of structures in the <b>Modules</b> array.


### -field Modules

An array of 
<a href="https://msdn.microsoft.com/17e32c6e-29df-4308-b22d-39e13bc6a2a5">MINIDUMP_MODULE</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/17e32c6e-29df-4308-b22d-39e13bc6a2a5">MINIDUMP_MODULE</a>



<a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a>
 

 

