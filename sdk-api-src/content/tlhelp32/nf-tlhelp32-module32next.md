---
UID: NF:tlhelp32.Module32Next
title: Module32Next function (tlhelp32.h)
description: The Module32Next function (tlhelp32.h) retrieves information about the next module associated with a process or thread.
helpviewer_keywords: ["Module32Next","Module32Next function [ToolHelp]","Module32NextW","_win32_module32next","base.module32next","tlhelp32/Module32Next","tlhelp32/Module32NextW","toolhelp.module32next"]
old-location: toolhelp\module32next.htm
tech.root: ToolHelp
ms.assetid: 88ec1af4-bae7-4cd7-b830-97a98fb337f4
ms.date: 08/05/2022
ms.keywords: Module32Next, Module32Next function [ToolHelp], Module32NextW, _win32_module32next, base.module32next, tlhelp32/Module32Next, tlhelp32/Module32NextW, toolhelp.module32next
req.header: tlhelp32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: Module32NextW (Unicode) and Module32Next (ANSI)
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
 - Module32Next
 - tlhelp32/Module32Next
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-toolhelp-l1-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
 - API-MS-Win-Core-ToolHelp-L1-1-1.dll
api_name:
 - Module32Next
 - Module32Next
 - Module32NextW
---

# Module32Next function


## -description

Retrieves information about the next module associated with a process or thread.

## -parameters

### -param hSnapshot [in]

A handle to the snapshot returned from a previous call to the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a> function.

### -param lpme [out]

A pointer to a 
<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-moduleentry32">MODULEENTRY32</a> structure.

## -returns

Returns <b>TRUE</b> if the next entry of the module list has been copied to the buffer or <b>FALSE</b> otherwise. The <b>ERROR_NO_MORE_FILES</b> error value is returned by the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function if no more modules exist.

## -remarks

To retrieve information about first module associated with a process, use the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-module32first">Module32First</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/ToolHelp/traversing-the-module-list">Traversing the Module List</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a>



<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-moduleentry32">MODULEENTRY32</a>



<a href="/windows/desktop/ToolHelp/module-walking">Module Walking</a>



<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-module32first">Module32First</a>



<a href="/windows/desktop/ToolHelp/tool-help-functions">Tool Help Functions</a>
