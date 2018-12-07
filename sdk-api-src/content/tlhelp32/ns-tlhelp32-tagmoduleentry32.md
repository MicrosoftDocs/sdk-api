---
UID: NS:tlhelp32.tagMODULEENTRY32
title: tagMODULEENTRY32
author: windows-sdk-content
description: Describes an entry from a list of the modules belonging to the specified process.
old-location: toolhelp\moduleentry32_str.htm
tech.root: ToolHelp
ms.assetid: 305fab35-625c-42e3-a434-e2513e4c8870
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPMODULEENTRY32, *PMODULEENTRY32, MODULEENTRY32, MODULEENTRY32 structure [ToolHelp], MODULEENTRY32W, PMODULEENTRY32, PMODULEENTRY32 structure pointer [ToolHelp], _win32_moduleentry32_str, base.moduleentry32_str, tagMODULEENTRY32, tlhelp32/MODULEENTRY32, tlhelp32/MODULEENTRY32W, tlhelp32/PMODULEENTRY32, toolhelp.moduleentry32_str"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: tlhelp32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MODULEENTRY32W (Unicode) and MODULEENTRY32 (ANSI)
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
 - TlHelp32.h
api_name:
 - MODULEENTRY32
 - MODULEENTRY32
 - MODULEENTRY32W
product: Windows
targetos: Windows
req.typenames: MODULEENTRY32
req.redist: 
---

# tagMODULEENTRY32 structure


## -description


Describes an entry from a list of the modules belonging to the specified process.


## -struct-fields




### -field dwSize

The size of the structure, in bytes. Before calling the 
<a href="https://msdn.microsoft.com/bb41cab9-13a1-469d-bf76-68c172e982f6">Module32First</a> function, set this member to <code>sizeof(MODULEENTRY32)</code>. If you do not initialize <b>dwSize</b>, 
<b>Module32First</b> fails.


### -field th32ModuleID

This member is no longer used, and is always set to one.


### -field th32ProcessID

The identifier of the process whose modules are to be examined.


### -field GlblcntUsage

The load count of the module, which is not generally meaningful, and usually equal to 0xFFFF.


### -field ProccntUsage

The load count of the module (same as <i>GlblcntUsage</i>), which is not generally meaningful, and usually equal to 0xFFFF.


### -field modBaseAddr

The base address of the module in the context of the owning process.


### -field modBaseSize

The size of the module, in bytes.


### -field hModule

A handle to the module in the context of the owning process.


### -field szModule

The module name.


### -field szExePath

The module path.


## -remarks



The <b>modBaseAddr</b> and <b>hModule</b> members are valid only in the context of the process specified by <i>th32ProcessID</i>.


#### Examples

For an example that uses <b>MODULEENTRY32</b>, see <a href="https://msdn.microsoft.com/8efe1e13-6222-496a-bff3-90f53b03c750">Traversing the Module List</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/bb41cab9-13a1-469d-bf76-68c172e982f6">Module32First</a>



<a href="https://msdn.microsoft.com/88ec1af4-bae7-4cd7-b830-97a98fb337f4">Module32Next</a>
 

 

