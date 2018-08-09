---
UID: NS:minidumpapiset._MINIDUMP_EXCEPTION_INFORMATION
title: "_MINIDUMP_EXCEPTION_INFORMATION"
author: windows-sdk-content
description: Contains the exception information written to the minidump file by the MiniDumpWriteDump function.
old-location: base\minidump_exception_information_str.htm
old-project: debug
ms.assetid: 86416432-99e4-45ae-84e0-84b7b2341d11
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PMINIDUMP_EXCEPTION_INFORMATION, MINIDUMP_EXCEPTION_INFORMATION, MINIDUMP_EXCEPTION_INFORMATION structure, PMINIDUMP_EXCEPTION_INFORMATION, PMINIDUMP_EXCEPTION_INFORMATION structure pointer, _MINIDUMP_EXCEPTION_INFORMATION, _win32_minidump_exception_information_str, base.minidump_exception_information_str, minidumpapiset/MINIDUMP_EXCEPTION_INFORMATION, minidumpapiset/PMINIDUMP_EXCEPTION_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: MINIDUMP_EXCEPTION_INFORMATION, *PMINIDUMP_EXCEPTION_INFORMATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_EXCEPTION_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MINIDUMP_EXCEPTION_INFORMATION structure


## -description


Contains the exception information written to the minidump file by the 
<a href="https://msdn.microsoft.com/b476023d-0e93-4d76-9ba8-ce5766c9ac51">MiniDumpWriteDump</a> function.


## -struct-fields




### -field ThreadId

The identifier of the thread throwing the exception.


### -field ExceptionPointers

A pointer to an 
<a href="https://msdn.microsoft.com/57e8cb3a-1b11-45b9-9676-3b6dc600d225">EXCEPTION_POINTERS</a> structure specifying a computer-independent description of the exception and the processor context at the time of the exception.


### -field ClientPointers

Determines where to get the memory regions pointed to by the <b>ExceptionPointers</b> member. Set to <b>TRUE</b> if the memory resides in the process being debugged (the target process of the debugger). Otherwise, set to <b>FALSE</b> if the memory resides in the address space of the calling program (the debugger process). If you are accessing local memory (in the calling process) you should not set this member to <b>TRUE</b>.


## -see-also




<a href="https://msdn.microsoft.com/57e8cb3a-1b11-45b9-9676-3b6dc600d225">EXCEPTION_POINTERS</a>



<a href="https://msdn.microsoft.com/b476023d-0e93-4d76-9ba8-ce5766c9ac51">MiniDumpWriteDump</a>
 

 

