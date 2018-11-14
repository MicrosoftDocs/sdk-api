---
UID: NS:minwinbase._LOAD_DLL_DEBUG_INFO
title: "_LOAD_DLL_DEBUG_INFO"
author: windows-sdk-content
description: Contains information about a dynamic-link library (DLL) that has just been loaded.
old-location: base\load_dll_debug_info_str.htm
tech.root: debug
ms.assetid: 80edb12f-1d1f-4480-9032-5f7a17f47910
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: "*LPLOAD_DLL_DEBUG_INFO, LOAD_DLL_DEBUG_INFO, LOAD_DLL_DEBUG_INFO structure, LPLOAD_DLL_DEBUG_INFO, LPLOAD_DLL_DEBUG_INFO structure pointer, _LOAD_DLL_DEBUG_INFO, _win32_load_dll_debug_info_str, base.load_dll_debug_info_str, minwinbase/LOAD_DLL_DEBUG_INFO, minwinbase/LPLOAD_DLL_DEBUG_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: minwinbase.h
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
 - minwinbase.h
api_name:
 - LOAD_DLL_DEBUG_INFO
product: Windows
targetos: Windows
req.typenames: LOAD_DLL_DEBUG_INFO, *LPLOAD_DLL_DEBUG_INFO
req.redist: 
---

# _LOAD_DLL_DEBUG_INFO structure


## -description


Contains information about a dynamic-link library (DLL) that has just been loaded.


## -struct-fields




### -field hFile

A handle to the loaded DLL. If this member is <b>NULL</b>, the handle is not valid. Otherwise, the member is opened for reading and read-sharing in the context of the debugger.

When the debugger is finished with this file, it should close the handle using the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.


### -field lpBaseOfDll

A pointer to the base address of the DLL in the address space of the process loading the DLL.


### -field dwDebugInfoFileOffset

The offset to the debugging information in the file identified by the <b>hFile</b> member, in bytes. The system expects the debugging information to be in CodeView 4.0 format. This format is currently a derivative of Common Object File Format (COFF).


### -field nDebugInfoSize

The size of the debugging information in the file, in bytes. If this member is zero, there is no debugging information.


### -field lpImageName

A pointer to the file name associated with <b>hFile</b>. This member may be <b>NULL</b>, or it may contain the address of a string pointer in the address space of the process being debugged. That address may, in turn, either be <b>NULL</b> or point to the actual filename. If <b>fUnicode</b> is a nonzero value, the name string is Unicode; otherwise, it is ANSI. 




This member is strictly optional. Debuggers must be prepared to handle the case where <b>lpImageName</b> is <b>NULL</b> or *<b>lpImageName</b> (in the address space of the process being debugged) is <b>NULL</b>. Specifically, the system will never provide an image name for a create process event, and it will not likely pass an image name for the first DLL event. The system will also never provide this information in the case of debugging events that originate from a call to the 
<a href="https://msdn.microsoft.com/306a5b28-658a-4dab-a516-c638b73f4a77">DebugActiveProcess</a> function.


### -field fUnicode

A value that indicates whether a filename specified by <b>lpImageName</b> is Unicode or ANSI. A nonzero value for this member indicates Unicode; zero indicates ANSI.


## -see-also




<a href="https://msdn.microsoft.com/4607aaff-bd05-46b5-86ed-abfffe6c2551">CREATE_PROCESS_DEBUG_INFO</a>



<a href="https://msdn.microsoft.com/daabd118-fa03-410e-af25-8655194902b0">CREATE_THREAD_DEBUG_INFO</a>



<a href="https://msdn.microsoft.com/056aa7ee-51ca-48ec-9cd7-26085bb85b11">DEBUG_EVENT</a>



<a href="https://msdn.microsoft.com/306a5b28-658a-4dab-a516-c638b73f4a77">DebugActiveProcess</a>
 

 

