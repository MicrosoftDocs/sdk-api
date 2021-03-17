---
UID: NS:minidumpapiset._MINIDUMP_EXCEPTION_INFORMATION
title: MINIDUMP_EXCEPTION_INFORMATION (minidumpapiset.h)
description: Contains the exception information written to the minidump file by the MiniDumpWriteDump function.
helpviewer_keywords: ["*PMINIDUMP_EXCEPTION_INFORMATION","MINIDUMP_EXCEPTION_INFORMATION","MINIDUMP_EXCEPTION_INFORMATION structure","PMINIDUMP_EXCEPTION_INFORMATION","PMINIDUMP_EXCEPTION_INFORMATION structure pointer","_MINIDUMP_EXCEPTION_INFORMATION","_win32_minidump_exception_information_str","base.minidump_exception_information_str","minidumpapiset/MINIDUMP_EXCEPTION_INFORMATION","minidumpapiset/PMINIDUMP_EXCEPTION_INFORMATION"]
old-location: base\minidump_exception_information_str.htm
tech.root: Debug
ms.assetid: 86416432-99e4-45ae-84e0-84b7b2341d11
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_EXCEPTION_INFORMATION, MINIDUMP_EXCEPTION_INFORMATION, MINIDUMP_EXCEPTION_INFORMATION structure, PMINIDUMP_EXCEPTION_INFORMATION, PMINIDUMP_EXCEPTION_INFORMATION structure pointer, _MINIDUMP_EXCEPTION_INFORMATION, _win32_minidump_exception_information_str, base.minidump_exception_information_str, minidumpapiset/MINIDUMP_EXCEPTION_INFORMATION, minidumpapiset/PMINIDUMP_EXCEPTION_INFORMATION'
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: MINIDUMP_EXCEPTION_INFORMATION, *PMINIDUMP_EXCEPTION_INFORMATION
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_EXCEPTION_INFORMATION
 - minidumpapiset/_MINIDUMP_EXCEPTION_INFORMATION
 - PMINIDUMP_EXCEPTION_INFORMATION
 - minidumpapiset/PMINIDUMP_EXCEPTION_INFORMATION
 - MINIDUMP_EXCEPTION_INFORMATION
 - minidumpapiset/MINIDUMP_EXCEPTION_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_EXCEPTION_INFORMATION
---

# MINIDUMP_EXCEPTION_INFORMATION structure


## -description

Contains the exception information written to the minidump file by the 
<a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a> function.

## -struct-fields

### -field ThreadId

The identifier of the thread throwing the exception.

### -field ExceptionPointers

A pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-exception_pointers">EXCEPTION_POINTERS</a> structure specifying a computer-independent description of the exception and the processor context at the time of the exception.

### -field ClientPointers

Determines where to get the memory regions pointed to by the <b>ExceptionPointers</b> member. Set to <b>TRUE</b> if the memory resides in the process being debugged (the target process of the debugger). Otherwise, set to <b>FALSE</b> if the memory resides in the address space of the calling program (the debugger process). If you are accessing local memory (in the calling process) you should not set this member to <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-exception_pointers">EXCEPTION_POINTERS</a>



<a href="/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a>