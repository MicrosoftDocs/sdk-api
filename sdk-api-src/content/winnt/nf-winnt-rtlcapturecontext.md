---
UID: NF:winnt.RtlCaptureContext
title: RtlCaptureContext function
author: windows-sdk-content
description: Retrieves a context record in the context of the caller.
old-location: base\rtlcapturecontext.htm
tech.root: debug
ms.assetid: e2ce0cde-43ab-4681-be66-bd7509fd6ca2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RtlCaptureContext, RtlCaptureContext function, base.rtlcapturecontext, winnt/RtlCaptureContext
ms.topic: function
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-rtlsupport-l1-1-0.dll
 - ntdll.dll
 - API-MS-Win-Core-rtlsupport-l1-2-0.dll
api_name:
 - RtlCaptureContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtlCaptureContext function


## -description


Retrieves a 
   context record in the context of the caller.


## -parameters




### -param ContextRecord [out]

A pointer to a <a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a> structure.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a>



<a href="https://msdn.microsoft.com/f5304d17-bc67-4e0f-a535-efca4e65c74c">RtlRestoreContext</a>
 

 

