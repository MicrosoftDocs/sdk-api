---
UID: NS:minidumpapiset._MINIDUMP_UNLOADED_MODULE
title: "_MINIDUMP_UNLOADED_MODULE"
author: windows-sdk-content
description: Contains information about a module that has been unloaded. This information can help diagnose problems calling code that is no longer loaded.
old-location: base\minidump_unloaded_module_str.htm
old-project: Debug
ms.assetid: d2ae58fa-561c-4135-a757-88598ebda57a
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*PMINIDUMP_UNLOADED_MODULE, MINIDUMP_UNLOADED_MODULE, MINIDUMP_UNLOADED_MODULE structure, PMINIDUMP_UNLOADED_MODULE, PMINIDUMP_UNLOADED_MODULE structure pointer, _MINIDUMP_UNLOADED_MODULE, _win32_minidump_unloaded_module_str, base.minidump_unloaded_module_str, minidumpapiset/MINIDUMP_UNLOADED_MODULE, minidumpapiset/PMINIDUMP_UNLOADED_MODULE"
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: MINIDUMP_UNLOADED_MODULE, *PMINIDUMP_UNLOADED_MODULE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	minidumpapiset.h
api_name:
-	MINIDUMP_UNLOADED_MODULE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MINIDUMP_UNLOADED_MODULE structure


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
<a href="https://msdn.microsoft.com/b90b2b29-9d39-4a73-b5fb-bb6e04c94811">MINIDUMP_STRING</a> structure that specifies the name of the module.


## -see-also




<a href="https://msdn.microsoft.com/26a42ae7-f84d-451d-92e9-dbaffb15ca74">MINIDUMP_UNLOADED_MODULE_LIST</a>
 

 

