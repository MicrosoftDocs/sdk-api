---
UID: NS:psapi._MODULEINFO
title: MODULEINFO (psapi.h)
description: Contains the module load address, size, and entry point.
helpviewer_keywords: ["*LPMODULEINFO","LPMODULEINFO","LPMODULEINFO structure pointer [PSAPI]","MODULEINFO","MODULEINFO structure [PSAPI]","_win32_moduleinfo_str","base.moduleinfo_str","psapi.moduleinfo_str","psapi/LPMODULEINFO","psapi/MODULEINFO"]
old-location: psapi\moduleinfo_str.htm
tech.root: psapi
ms.assetid: 583caafe-7fa3-4041-b5bc-4e8899b3a08a
ms.date: 12/05/2018
ms.keywords: '*LPMODULEINFO, LPMODULEINFO, LPMODULEINFO structure pointer [PSAPI], MODULEINFO, MODULEINFO structure [PSAPI], _win32_moduleinfo_str, base.moduleinfo_str, psapi.moduleinfo_str, psapi/LPMODULEINFO, psapi/MODULEINFO'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MODULEINFO, *LPMODULEINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MODULEINFO
 - psapi/_MODULEINFO
 - LPMODULEINFO
 - psapi/LPMODULEINFO
 - MODULEINFO
 - psapi/MODULEINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Psapi.h
api_name:
 - MODULEINFO
---

# MODULEINFO structure


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
<a href="/windows/desktop/Dlls/dllmain">DllMain</a> function, it should be close enough for most purposes.

## -see-also

<a href="/windows/desktop/api/psapi/nf-psapi-getmoduleinformation">GetModuleInformation</a>