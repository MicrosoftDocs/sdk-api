---
UID: NF:tlhelp32.Thread32First
title: Thread32First function (tlhelp32.h)
description: Retrieves information about the first thread of any process encountered in a system snapshot.
helpviewer_keywords: ["Thread32First","Thread32First function [ToolHelp]","_win32_thread32first","base.thread32first","tlhelp32/Thread32First","toolhelp.thread32first"]
old-location: toolhelp\thread32first.htm
tech.root: ToolHelp
ms.assetid: d4cb7a19-850e-43b5-bda5-91be48382d2a
ms.date: 12/05/2018
ms.keywords: Thread32First, Thread32First function [ToolHelp], _win32_thread32first, base.thread32first, tlhelp32/Thread32First, toolhelp.thread32first
req.header: tlhelp32.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Thread32First
 - tlhelp32/Thread32First
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-toolhelp-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-ToolHelp-L1-1-1.dll
api_name:
 - Thread32First
---

# Thread32First function


## -description

Retrieves information about the first thread of any process encountered in a system snapshot.

## -parameters

### -param hSnapshot [in]

A handle to the snapshot returned from a previous call to the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a> function.

### -param lpte [in, out]

A pointer to a 
<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-threadentry32">THREADENTRY32</a> structure.

## -returns

Returns <b>TRUE</b> if the first entry of the thread list has been copied to the buffer or <b>FALSE</b> otherwise. The <b>ERROR_NO_MORE_FILES</b> error value is returned by the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function if no threads exist or the snapshot does not contain thread information.

## -remarks

The calling application must set the <b>dwSize</b> member of 
<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-threadentry32">THREADENTRY32</a> to the size, in bytes, of the structure. 
<b>Thread32First</b> changes <b>dwSize</b> to the number of bytes written to the structure. This will never be greater than the initial value of <b>dwSize</b>, but it may be smaller. If the value is smaller, do not rely on the values of any members whose offsets are greater than this value.

To retrieve information about other threads recorded in the same snapshot, use the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-thread32next">Thread32Next</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/ToolHelp/traversing-the-thread-list">Traversing the Thread List</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a>



<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-threadentry32">THREADENTRY32</a>



<a href="/windows/desktop/ToolHelp/thread-walking">Thread Walking</a>



<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-thread32next">Thread32Next</a>



<a href="/windows/desktop/ToolHelp/tool-help-functions">Tool Help Functions</a>