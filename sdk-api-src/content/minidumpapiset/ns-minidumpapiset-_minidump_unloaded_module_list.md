---
UID: NS:minidumpapiset._MINIDUMP_UNLOADED_MODULE_LIST
title: "_MINIDUMP_UNLOADED_MODULE_LIST"
author: windows-sdk-content
description: Contains a list of unloaded modules.
old-location: base\minidump_unloaded_module_list_str.htm
old-project: Debug
ms.assetid: 26a42ae7-f84d-451d-92e9-dbaffb15ca74
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*PMINIDUMP_UNLOADED_MODULE_LIST, MINIDUMP_UNLOADED_MODULE_LIST, MINIDUMP_UNLOADED_MODULE_LIST structure, PMINIDUMP_UNLOADED_MODULE_LIST, PMINIDUMP_UNLOADED_MODULE_LIST structure pointer, _MINIDUMP_UNLOADED_MODULE_LIST, _win32_minidump_unloaded_module_list_str, base.minidump_unloaded_module_list_str, minidumpapiset/MINIDUMP_UNLOADED_MODULE_LIST, minidumpapiset/PMINIDUMP_UNLOADED_MODULE_LIST"
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
tech.root: 
req.typenames: MINIDUMP_UNLOADED_MODULE_LIST, *PMINIDUMP_UNLOADED_MODULE_LIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_UNLOADED_MODULE_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MINIDUMP_UNLOADED_MODULE_LIST structure


## -description


Contains a list of unloaded modules.


## -struct-fields




### -field SizeOfHeader

The size of the header data for the stream, in bytes. This is generally <code>sizeof(MINIDUMP_UNLOADED_MODULE_LIST)</code>.


### -field SizeOfEntry

The size of each entry following the header, in bytes. This is generally <code>sizeof(MINIDUMP_UNLOADED_MODULE)</code>.


### -field NumberOfEntries

The number of entries in the stream. These are generally <a href="https://msdn.microsoft.com/d2ae58fa-561c-4135-a757-88598ebda57a">MINIDUMP_UNLOADED_MODULE</a> structures. The entries follow the header.


## -see-also




<a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a>



<a href="https://msdn.microsoft.com/d2ae58fa-561c-4135-a757-88598ebda57a">MINIDUMP_UNLOADED_MODULE</a>
 

 

