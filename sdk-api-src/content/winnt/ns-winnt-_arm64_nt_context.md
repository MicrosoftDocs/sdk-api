---
UID: NS:winnt._ARM64_NT_CONTEXT
title: "_ARM64_NT_CONTEXT"
author: windows-sdk-content
description: Contains processor-specific register data. The system uses CONTEXT structures to perform various internal operations.
old-location: base\context_str.htm
tech.root: debug
ms.assetid: a6c201b3-4402-4de4-89c7-e6e2fbcd27f7
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*PARM64_NT_CONTEXT, *PCONTEXT, ARM64_NT_CONTEXT, CONTEXT, CONTEXT structure, LPCONTEXT, LPCONTEXT structure pointer, _ARM64_NT_CONTEXT, _win32_context_str, base.context_str, winnt/CONTEXT, winnt/LPCONTEXT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: ARM64_NT_CONTEXT, *PARM64_NT_CONTEXT
req.redist: 
---

# _ARM64_NT_CONTEXT structure


## -description


Contains processor-specific register data. The system uses 
   <b>CONTEXT</b> structures to perform various internal 
   operations. Refer to the header file WinNT.h for definitions of this structure for each 
   processor architecture.


## -struct-fields


## -see-also




<a href="https://msdn.microsoft.com/bf1294cd-1836-49d3-9cc4-4532429a301f">Debugging Structures</a>



<a href="https://msdn.microsoft.com/3b65283e-34d2-4374-87fe-fa8ae45fbbcf">GetThreadContext</a>



<a href="https://msdn.microsoft.com/D9A8D0B6-21E3-46B7-AB88-CE2FF4025A17">GetXStateFeaturesMask</a>



<a href="https://msdn.microsoft.com/be134953-b569-48ea-80ac-ab14dee24500">SetThreadContext</a>



<a href="https://msdn.microsoft.com/b27205a2-2c33-4f45-8948-9919bcd2355a">WOW64_CONTEXT</a>
 

 

