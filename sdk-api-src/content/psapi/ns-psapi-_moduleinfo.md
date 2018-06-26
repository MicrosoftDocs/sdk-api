---
UID: NS:psapi._MODULEINFO
title: "_MODULEINFO"
author: windows-sdk-content
description: Contains the module load address, size, and entry point.
old-location: psapi\moduleinfo_str.htm
old-project: psapi
ms.assetid: 583caafe-7fa3-4041-b5bc-4e8899b3a08a
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: "*LPMODULEINFO, LPMODULEINFO, LPMODULEINFO structure pointer [PSAPI], MODULEINFO, MODULEINFO structure [PSAPI], _MODULEINFO, _win32_moduleinfo_str, base.moduleinfo_str, psapi.moduleinfo_str, psapi/LPMODULEINFO, psapi/MODULEINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: MODULEINFO, *LPMODULEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Psapi.h
api_name:
 - MODULEINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _MODULEINFO structure


## -description


Contains the module load address, size, and entry point.


## -struct-fields




### -field lpBaseOfDll

The load address of the module.


### -field SizeOfImage

The size of the linear space that the module occupies, in bytes.


### -field EntryPoint

The entry point of the module.


## -remarks



The load address of a module is the same as the <b>HMODULE</b> value. The information returned in the <b>SizeOfImage</b> and <b>EntryPoint</b> members comes from the module's Portable Executable (PE) header. The module entry point is the location called during process startup, thread startup, process shutdown, and thread shutdown. While this is not the address of the 
<a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> function, it should be close enough for most purposes.




## -see-also




<a href="https://msdn.microsoft.com/afb9f4c8-c8ae-4497-96c1-b559cfa2cedf">GetModuleInformation</a>
 

 

