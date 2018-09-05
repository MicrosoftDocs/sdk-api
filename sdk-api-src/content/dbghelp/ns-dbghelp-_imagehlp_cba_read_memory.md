---
UID: NS:dbghelp._IMAGEHLP_CBA_READ_MEMORY
title: "_IMAGEHLP_CBA_READ_MEMORY"
author: windows-sdk-content
description: Contains information about a memory read operation.
old-location: base\imagehlp_cba_read_memory_str.htm
old-project: debug
ms.assetid: c5115fdc-aca6-4293-9c2b-82fd64ec7cb6
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: "*PIMAGEHLP_CBA_READ_MEMORY, IMAGEHLP_CBA_READ_MEMORY, IMAGEHLP_CBA_READ_MEMORY structure, PIMAGEHLP_CBA_READ_MEMORY, PIMAGEHLP_CBA_READ_MEMORY structure pointer, _IMAGEHLP_CBA_READ_MEMORY, _win32_imagehlp_cba_read_memory_str, base.imagehlp_cba_read_memory_str, dbghelp/IMAGEHLP_CBA_READ_MEMORY, dbghelp/PIMAGEHLP_CBA_READ_MEMORY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dbghelp.h
req.include-header: 
req.redist: DbgHelp.dll 5.1 or later
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
req.typenames: IMAGEHLP_CBA_READ_MEMORY, *PIMAGEHLP_CBA_READ_MEMORY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DbgHelp.h
api_name:
 - IMAGEHLP_CBA_READ_MEMORY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _IMAGEHLP_CBA_READ_MEMORY structure


## -description


Contains information about a memory read operation.


## -struct-fields




### -field addr

The address to be read.


### -field buf

A pointer to a buffer that receives the memory read.


### -field bytes

The number of bytes to read.


### -field bytesread

A pointer to a variable that receives the number of bytes read.


## -see-also




<a href="https://msdn.microsoft.com/f3ba952b-ecc5-4235-a806-00c82d40e611">SymRegisterCallbackProc64</a>
 

 

