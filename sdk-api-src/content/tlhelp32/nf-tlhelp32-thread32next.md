---
UID: NF:tlhelp32.Thread32Next
title: Thread32Next function (tlhelp32.h)
description: Retrieves information about the next thread of any process encountered in the system memory snapshot.
helpviewer_keywords: ["Thread32Next","Thread32Next function [ToolHelp]","_win32_thread32next","base.thread32next","tlhelp32/Thread32Next","toolhelp.thread32next"]
old-location: toolhelp\thread32next.htm
tech.root: ToolHelp
ms.assetid: 5efe514e-626c-4138-97a0-bdad217c424f
ms.date: 12/05/2018
ms.keywords: Thread32Next, Thread32Next function [ToolHelp], _win32_thread32next, base.thread32next, tlhelp32/Thread32Next, toolhelp.thread32next
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
 - Thread32Next
 - tlhelp32/Thread32Next
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
 - Thread32Next
---

# Thread32Next function


## -description

Retrieves information about the next thread of any process encountered in the system memory snapshot.

## -parameters

### -param hSnapshot [in]

A handle to the snapshot returned from a previous call to the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a> function.

### -param lpte [out]

A pointer to a 
<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-threadentry32">THREADENTRY32</a> structure.

## -returns

Returns <b>TRUE</b> if the next entry of the thread list has been copied to the buffer or <b>FALSE</b> otherwise. The <b>ERROR_NO_MORE_FILES</b> error value is returned by the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function if no threads exist or the snapshot does not contain thread information.

## -remarks

To retrieve information about the first thread recorded in a snapshot, use the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-thread32first">Thread32First</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/ToolHelp/traversing-the-thread-list">Traversing the Thread List</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-createtoolhelp32snapshot">CreateToolhelp32Snapshot</a>



<a href="/windows/desktop/api/tlhelp32/ns-tlhelp32-threadentry32">THREADENTRY32</a>



<a href="/windows/desktop/ToolHelp/thread-walking">Thread Walking</a>



<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-thread32first">Thread32First</a>



<a href="/windows/desktop/ToolHelp/tool-help-functions">Tool Help Functions</a>