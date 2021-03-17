---
UID: NS:tlhelp32.tagTHREADENTRY32
title: THREADENTRY32 (tlhelp32.h)
description: Describes an entry from a list of the threads executing in the system when a snapshot was taken.
helpviewer_keywords: ["*LPTHREADENTRY32","*PTHREADENTRY32","PTHREADENTRY32","PTHREADENTRY32 structure pointer [ToolHelp]","THREADENTRY32","THREADENTRY32 structure [ToolHelp]","_win32_threadentry32_str","base.threadentry32_str","tlhelp32/PTHREADENTRY32","tlhelp32/THREADENTRY32","toolhelp.threadentry32_str"]
old-location: toolhelp\threadentry32_str.htm
tech.root: ToolHelp
ms.assetid: 923feca1-8807-4752-8a5a-79075688aabd
ms.date: 12/05/2018
ms.keywords: '*LPTHREADENTRY32, *PTHREADENTRY32, PTHREADENTRY32, PTHREADENTRY32 structure pointer [ToolHelp], THREADENTRY32, THREADENTRY32 structure [ToolHelp], _win32_threadentry32_str, base.threadentry32_str, tlhelp32/PTHREADENTRY32, tlhelp32/THREADENTRY32, toolhelp.threadentry32_str'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: THREADENTRY32
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTHREADENTRY32
 - tlhelp32/tagTHREADENTRY32
 - THREADENTRY32
 - tlhelp32/THREADENTRY32
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
 - THREADENTRY32
---

# THREADENTRY32 structure


## -description

Describes an entry from a list of the threads executing in the system when a snapshot was taken.

## -struct-fields

### -field dwSize

The size of the structure, in bytes. Before calling the 
<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-thread32first">Thread32First</a> function, set this member to <code>sizeof(THREADENTRY32)</code>. If you do not initialize <b>dwSize</b>, 
<b>Thread32First</b> fails.

### -field cntUsage

This member is no longer used and is always set to zero.

### -field th32ThreadID

The thread identifier, compatible with the thread identifier returned by the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> function.

### -field th32OwnerProcessID

The identifier of the process that created the thread.

### -field tpBasePri

The kernel base priority level assigned to the thread. The priority is a number from 0 to 31, with 0 representing the lowest possible thread priority. For more information, see <b>KeQueryPriorityThread</b>.

### -field tpDeltaPri

This member is no longer used and is always set to zero.

### -field dwFlags

This member is no longer used and is always set to zero.

## -see-also

<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-thread32first">Thread32First</a>



<a href="/windows/desktop/api/tlhelp32/nf-tlhelp32-thread32next">Thread32Next</a>