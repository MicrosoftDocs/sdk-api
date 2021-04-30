---
UID: NF:tlhelp32.Module32FirstW
title: Module32FirstW function (tlhelp32.h)
description: Retrieves information about the first module associated with a process.
helpviewer_keywords: ["Module32First","Module32First function [ToolHelp]","Module32FirstW","_win32_module32first","base.module32first","tlhelp32/Module32First","tlhelp32/Module32FirstW","toolhelp.module32first"]
old-location: toolhelp\module32first.htm
tech.root: ToolHelp
ms.assetid: bb41cab9-13a1-469d-bf76-68c172e982f6
ms.date: 12/05/2018
ms.keywords: Module32First, Module32First function [ToolHelp], Module32FirstW, _win32_module32first, base.module32first, tlhelp32/Module32First, tlhelp32/Module32FirstW, toolhelp.module32first
req.header: tlhelp32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: Module32FirstW (Unicode) and Module32First (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Module32FirstW
 - tlhelp32/Module32FirstW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-toolhelp-l1-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
 - API-MS-Win-Core-ToolHelp-L1-1-1.dll
api_name:
 - Module32First
 - Module32First
 - Module32FirstW
---

# Module32FirstW function


## -description

Retrieves information about the first module associated with a process.

## -parameters

### -param hSnapshot [in]

A handle to the snapshot returned from a previous call to the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a> function.

### -param lpme [in, out]

A pointer to a 
<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-moduleentry32w">MODULEENTRY32W</a> structure.

## -returns

Returns <b>TRUE</b> if the first entry of the module list has been copied to the buffer or <b>FALSE</b> otherwise. The <b>ERROR_NO_MORE_FILES</b> error value is returned by the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function if no modules exist or the snapshot does not contain module information.

## -remarks

The calling application must set the <b>dwSize</b> member of 
<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-moduleentry32w">MODULEENTRY32W</a> to the size, in bytes, of the structure.

To retrieve information about other modules associated with the specified process, use the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-module32nextw">Module32NextW</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/ToolHelp/traversing-the-module-list">Traversing the Module List</a>.

<div class="code"></div>




> [!NOTE]
> The tlhelp32.h header defines Module32First as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a>



<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-moduleentry32w">MODULEENTRY32W</a>



<a href="/windows/desktop/ToolHelp/module-walking">Module Walking</a>



<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-module32nextw">Module32NextW</a>



<a href="/windows/desktop/ToolHelp/tool-help-functions">Tool Help Functions</a>