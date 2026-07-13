---
UID: NS:winnt._CONTEXT
title: CONTEXT (x86 64-bit)
description: Contains processor-specific register data for 64-bit x86 architecture. The system uses CONTEXT structures to perform various internal operations.
helpviewer_keywords: ["*PCONTEXT","CONTEXT","CONTEXT structure","LPCONTEXT","LPCONTEXT structure pointer","_win32_context_str","base.context_str","winnt/CONTEXT","winnt/LPCONTEXT"]
old-location: base\context_str.htm
tech.root: Debug
ms.assetid: a6c201b3-4402-4de4-89c7-e6e2fbcd27f7
ms.date: 12/05/2018
ms.keywords: '*PCONTEXT, CONTEXT, CONTEXT structure, LPCONTEXT, LPCONTEXT structure pointer, _win32_context_str, base.context_str, winnt/CONTEXT, winnt/LPCONTEXT'
req.header: winnt.h
req.include-header: Windows.h
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
req.typenames: CONTEXT, *PCONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CONTEXT
 - winnt/_CONTEXT
 - PCONTEXT
 - winnt/PCONTEXT
 - CONTEXT
 - winnt/CONTEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - CONTEXT
h1-override: CONTEXT structure (x86 64-bit)
---

# CONTEXT structure (x86 64-bit)


## -description

Contains processor-specific register data. The system uses <b>CONTEXT</b> structures to perform various internal operations. The structure definition varies for different processor architectures. This page applies to the 64-bit x86 architecture. The following table links to the structures for other architectures.

| Architecture | API reference page |
|--------------|--------------------|
| x86 32-bit | [CONTEXT structure (x86 32-bit)](ns-winnt-context~r2.md) |
| Arm32 | [CONTEXT structure (Arm32)](ns-winnt-context~r1.md) |
| Arm64 | [ARM64_NT_CONTEXT structure](ns-winnt-arm64_nt_context.md) |



## -struct-fields

## -see-also

<a href="/windows/desktop/Debug/debugging-structures">Debugging Structures</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadcontext">GetThreadContext</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getxstatefeaturesmask">GetXStateFeaturesMask</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext">SetThreadContext</a>



<a href="/windows/desktop/api/winnt/ns-winnt-wow64_context">WOW64_CONTEXT</a>
