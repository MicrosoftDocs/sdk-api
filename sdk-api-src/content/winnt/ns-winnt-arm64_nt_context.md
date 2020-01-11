---
UID: NS:winnt._ARM64_NT_CONTEXT
title: ARM64_NT_CONTEXT (winnt.h)
description: Contains processor-specific register data. The system uses CONTEXT structures to perform various internal operations.
old-location: base\context_str.htm
tech.root: Debug
ms.assetid: a6c201b3-4402-4de4-89c7-e6e2fbcd27f7
ms.date: 12/05/2018
ms.keywords: '*PARM64_NT_CONTEXT, *PCONTEXT, ARM64_NT_CONTEXT, CONTEXT, CONTEXT structure, LPCONTEXT, LPCONTEXT structure pointer, _win32_context_str, base.context_str, winnt/CONTEXT, winnt/LPCONTEXT'
f1_keywords:
- winnt/CONTEXT
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- WinNT.h
api_name:
- CONTEXT
targetos: Windows
req.typenames: ARM64_NT_CONTEXT, *PARM64_NT_CONTEXT
req.redist: 
ms.custom: 19H1
---

# ARM64_NT_CONTEXT structure


## -description


Contains processor-specific register data. The system uses 
   <b>CONTEXT</b> structures to perform various internal 
   operations. Refer to the header file WinNT.h for definitions of this structure for each 
   processor architecture.


## -struct-fields


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/debugging-structures">Debugging Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getthreadcontext">GetThreadContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getxstatefeaturesmask">GetXStateFeaturesMask</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setthreadcontext">SetThreadContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-wow64_context">WOW64_CONTEXT</a>
 

 

