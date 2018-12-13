---
UID: NS:winnt._EXCEPTION_POINTERS
title: EXCEPTION_POINTERS
author: windows-sdk-content
description: Contains an exception record with a machine-independent description of an exception and a context record with a machine-dependent description of the processor context at the time of the exception.
old-location: base\exception_pointers_str.htm
tech.root: debug
ms.assetid: 57e8cb3a-1b11-45b9-9676-3b6dc600d225
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PEXCEPTION_POINTERS, EXCEPTION_POINTERS, EXCEPTION_POINTERS structure, PEXCEPTION_POINTERS, PEXCEPTION_POINTERS structure pointer, _EXCEPTION_POINTERS, _win32_exception_pointers_str, base.exception_pointers_str, winnt/EXCEPTION_POINTERS, winnt/PEXCEPTION_POINTERS"
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
 - EXCEPTION_POINTERS
product: Windows
targetos: Windows
req.typenames: EXCEPTION_POINTERS, *PEXCEPTION_POINTERS
req.redist: 
---

# EXCEPTION_POINTERS structure


## -description


Contains an exception record with a machine-independent description of an exception and a context record with a machine-dependent description of the processor context at the time of the exception.


## -struct-fields




### -field ExceptionRecord

A pointer to an 
<a href="https://msdn.microsoft.com/85a64178-bdcb-4293-9363-289c654730a2">EXCEPTION_RECORD</a> structure that contains a machine-independent description of the exception.


### -field ContextRecord

A pointer to a 
<a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a> structure that contains a processor-specific description of the state of the processor at the time of the exception.


## -see-also




<a href="https://msdn.microsoft.com/a6c201b3-4402-4de4-89c7-e6e2fbcd27f7">CONTEXT</a>



<a href="https://msdn.microsoft.com/85a64178-bdcb-4293-9363-289c654730a2">EXCEPTION_RECORD</a>



<a href="https://msdn.microsoft.com/e982794a-d5f1-4fb4-a2b9-aa8da18cb8ae">GetExceptionInformation</a>
 

 

