---
UID: NS:tlhelp32.tagMODULEENTRY32W
title: MODULEENTRY32W (tlhelp32.h)
description: Describes an entry from a list of the modules belonging to the specified process.helpviewer_keywords: ["*LPMODULEENTRY32W","*PMODULEENTRY32W","MODULEENTRY32","MODULEENTRY32 structure [ToolHelp]","MODULEENTRY32W","PMODULEENTRY32","PMODULEENTRY32 structure pointer [ToolHelp]","_win32_moduleentry32_str","base.moduleentry32_str","tlhelp32/MODULEENTRY32","tlhelp32/MODULEENTRY32W","tlhelp32/PMODULEENTRY32","toolhelp.moduleentry32_str"]
old-location: toolhelp\moduleentry32_str.htm
tech.root: ToolHelp
ms.assetid: 305fab35-625c-42e3-a434-e2513e4c8870
ms.date: 12/05/2018
ms.keywords: '*LPMODULEENTRY32W, *PMODULEENTRY32W, MODULEENTRY32, MODULEENTRY32 structure [ToolHelp], MODULEENTRY32W, PMODULEENTRY32, PMODULEENTRY32 structure pointer [ToolHelp], _win32_moduleentry32_str, base.moduleentry32_str, tlhelp32/MODULEENTRY32, tlhelp32/MODULEENTRY32W, tlhelp32/PMODULEENTRY32, toolhelp.moduleentry32_str'
f1_keywords:
- tlhelp32/MODULEENTRY32
dev_langs:
- c++
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
targetos: Windows
req.typenames: MODULEENTRY32W
req.redist: 
ms.custom: 19H1
---

# MODULEENTRY32W structure


## -description


Describes an entry from a list of the modules belonging to the specified process.


## -struct-fields




### -field dwSize

The size of the structure, in bytes. Before calling the 
<a href="https://docs.microsoft.com/windows/desktop/api/tlhelp32/nf-tlhelp32-module32first">Module32First</a> function, set this member to <code>sizeof(MODULEENTRY32)</code>. If you do not initialize <b>dwSize</b>, 
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

For an example that uses <b>MODULEENTRY32</b>, see <a href="https://docs.microsoft.com/windows/desktop/ToolHelp/traversing-the-module-list">Traversing the Module List</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tlhelp32/nf-tlhelp32-module32first">Module32First</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tlhelp32/nf-tlhelp32-module32next">Module32Next</a>
 

 

