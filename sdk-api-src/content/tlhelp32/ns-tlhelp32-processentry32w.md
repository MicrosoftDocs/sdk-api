---
UID: NS:tlhelp32.tagPROCESSENTRY32W
title: PROCESSENTRY32W (tlhelp32.h)
description: The PROCESSENTRY32W (Unicode) structure (tlhelp32.h) describes an entry from a list of the processes residing in the system address space when a snapshot was taken.
helpviewer_keywords: ["*LPPROCESSENTRY32W","*PPROCESSENTRY32W","PPROCESSENTRY32","PPROCESSENTRY32 structure pointer [ToolHelp]","PROCESSENTRY32","PROCESSENTRY32 structure [ToolHelp]","PROCESSENTRY32W","_win32_processentry32_str","base.processentry32_str","tlhelp32/PPROCESSENTRY32","tlhelp32/PROCESSENTRY32","tlhelp32/PROCESSENTRY32W","toolhelp.processentry32_str"]
old-location: toolhelp\processentry32_str.htm
tech.root: ToolHelp
ms.assetid: 9e2f7345-52bf-4bfc-9761-90b0b374c727
ms.date: 08/05/2022
ms.keywords: '*LPPROCESSENTRY32W, *PPROCESSENTRY32W, PPROCESSENTRY32, PPROCESSENTRY32 structure pointer [ToolHelp], PROCESSENTRY32, PROCESSENTRY32 structure [ToolHelp], PROCESSENTRY32W, _win32_processentry32_str, base.processentry32_str, tlhelp32/PPROCESSENTRY32, tlhelp32/PROCESSENTRY32, tlhelp32/PROCESSENTRY32W, toolhelp.processentry32_str'
req.header: tlhelp32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PROCESSENTRY32W (Unicode) and PROCESSENTRY32 (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PROCESSENTRY32W
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPROCESSENTRY32W
 - tlhelp32/tagPROCESSENTRY32W
 - PROCESSENTRY32W
 - tlhelp32/PROCESSENTRY32W
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - TlHelp32.h
api_name:
 - PROCESSENTRY32
 - PROCESSENTRY32
 - PROCESSENTRY32W
---

# PROCESSENTRY32W structure


## -description

Describes an entry from a list of the processes residing in the system address space when a snapshot was taken.

## -struct-fields

### -field dwSize

The size of the structure, in bytes. Before calling the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-process32first">Process32First</a> function, set this member to <code>sizeof(PROCESSENTRY32)</code>. If you do not initialize <b>dwSize</b>, 
<b>Process32First</b> fails.

### -field cntUsage

This member is no longer used and is always set to zero.

### -field th32ProcessID

The process identifier.

### -field th32DefaultHeapID

This member is no longer used and is always set to zero.

### -field th32ModuleID

This member is no longer used and is always set to zero.

### -field cntThreads

The number of execution threads started by the process.

### -field th32ParentProcessID

The identifier of the process that created this process (its parent process).

### -field pcPriClassBase

The base priority of any threads created by this process.

### -field dwFlags

This member is no longer used, and is always set to zero.

### -field szExeFile

The name of the executable file for the process. To retrieve the full path to the executable file, call the <a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-module32first">Module32First</a> function and check the <b>szExePath</b> member of the <a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-moduleentry32">MODULEENTRY32</a> structure that is returned. However, if the calling process is a 32-bit process, you must call the <a href="/windows/desktop/api/winbase/nf-winbase-queryfullprocessimagenamea">QueryFullProcessImageName</a> function to retrieve the full path of the executable file for a 64-bit process.

## -see-also

<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-process32first">Process32First</a>



<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-process32next">Process32Next</a>

## -remarks

> [!NOTE]
> The tlhelp32.h header defines PROCESSENTRY32 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
