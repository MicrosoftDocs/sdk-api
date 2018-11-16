---
UID: NF:dbghelp.MapDebugInformation
title: MapDebugInformation function
author: windows-sdk-content
description: Obtains access to the debugging information for an image.
old-location: base\mapdebuginformation.htm
tech.root: Debug
ms.assetid: 749a2a99-f6c4-4af3-aa0b-8a7bb5c690da
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MapDebugInformation, MapDebugInformation function, _win32_mapdebuginformation, base.mapdebuginformation, dbghelp/MapDebugInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dbghelp.h
req.include-header: 
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
req.lib: Dbghelp.lib
req.dll: Dbghelp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dbghelp.dll
api_name:
 - MapDebugInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
- apiref
: 
- 
: 
- MapDebugInformation
: 
---

# MapDebugInformation function


## -description


Obtains access to the debugging information for an image.
<div class="alert"><b>Note</b>  This function is provided only for backward compatibility. It does not return reliable information. New applications should use the 
<a href="https://msdn.microsoft.com/e8057cb5-3331-4460-b07c-4338a57024be">SymGetModuleInfo64</a> and 
<a href="https://msdn.microsoft.com/be50588b-066b-42ab-ba81-7537c811676f">SymLoadModule64</a> functions. </div><div> </div>

## -parameters




### -param FileHandle [in, optional]

A handle to an open executable image or <b>NULL</b>.


### -param FileName [in]

The name of an executable image file or <b>NULL</b>.


### -param SymbolPath [in, optional]

The path where symbol files are located. The path can be multiple paths separated by semicolons. To retrieve the symbol path, use the 
<a href="https://msdn.microsoft.com/aa8c8450-ee67-4614-98a1-5feebdd3a788">SymGetSearchPath</a> function.


### -param ImageBase [in]

The base address for the image or zero.


## -returns



If the function succeeds, the return value is a pointer to an 
<a href="https://msdn.microsoft.com/f8db7695-4967-45c0-a6bf-019e825bd9ab">IMAGE_DEBUG_INFORMATION</a> structure.

If the function fails, the return value is <b>NULL</b>. To retrieve extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>MapDebugInformation</b> function is used to obtain access to an image's debugging information. The debugging information is extracted from the image or the symbol file and placed into the 
<a href="https://msdn.microsoft.com/f8db7695-4967-45c0-a6bf-019e825bd9ab">IMAGE_DEBUG_INFORMATION</a> structure. This structure is allocated by the library and must be deallocated by using the 
<a href="https://msdn.microsoft.com/86d82f23-7803-475f-8b23-c3964d33cb00">UnmapDebugInformation</a> function. The memory for the structure is not in the process's default heap, so attempts to free it with a memory deallocation routine will fail.

All DbgHelp functions, such as this one, are single threaded. Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption. To avoid this, you must synchronize all concurrent calls from more than one thread to this function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/f8db7695-4967-45c0-a6bf-019e825bd9ab">IMAGE_DEBUG_INFORMATION</a>



<a href="https://msdn.microsoft.com/aa8c8450-ee67-4614-98a1-5feebdd3a788">SymGetSearchPath</a>



<a href="https://msdn.microsoft.com/86d82f23-7803-475f-8b23-c3964d33cb00">UnmapDebugInformation</a>
 

 

