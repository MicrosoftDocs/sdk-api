---
UID: NF:psapi.GetModuleFileNameExA
title: GetModuleFileNameExA function
author: windows-sdk-content
description: Retrieves the fully qualified path for the file containing the specified module.
old-location: psapi\getmodulefilenameex.htm
old-project: psapi
ms.assetid: 4199ce12-e82f-4a58-ac66-e0ddc0dffbff
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetModuleFileNameEx, GetModuleFileNameEx function [PSAPI], GetModuleFileNameExA, GetModuleFileNameExW, K32GetModuleFileNameEx, K32GetModuleFileNameExA, K32GetModuleFileNameExW, _win32_getmodulefilenameex, base.getmodulefilenameex, psapi.getmodulefilenameex, psapi/GetModuleFileNameEx, psapi/GetModuleFileNameExA, psapi/GetModuleFileNameExW, psapi/K32GetModuleFileNameEx, psapi/K32GetModuleFileNameExA, psapi/K32GetModuleFileNameExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetModuleFileNameExW (Unicode) and GetModuleFileNameExA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PSHNOTIFY, *LPPSHNOTIFY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - Psapi.dll
 - Psapi.dll
 - API-MS-Win-Core-PsAPI-Obsolete-L1-1-0.dll
 - KernelBase.dll
 - API-Ms-Win-Core-PsAPI-Ansi-L1-1-0.dll
 - API-Ms-Win-Core-PsAPI-L1-1-0.dll
api_name:
 - GetModuleFileNameEx
 - GetModuleFileNameExA
 - GetModuleFileNameExW
 - K32GetModuleFileNameEx
 - K32GetModuleFileNameExW
 - K32GetModuleFileNameExA
product: Windows
targetos: Windows
req.lib: Kernel32.lib on Windows 7 and Windows Server 2008 R2; Psapi.lib (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.lib on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.dll: Kernel32.dll on Windows 7 and Windows Server 2008 R2; Psapi.dll (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.irql: 
req.product: ADAM
---

# GetModuleFileNameExA function


## -description


Retrieves the fully qualified path for the file containing the specified module.


## -parameters




### -param hProcess [in]

A handle to the process that contains the module.  

The handle must have the <b>PROCESS_QUERY_INFORMATION</b> and <b>PROCESS_VM_READ</b> access rights. For more information, see <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.

The <b>GetModuleFileNameEx</b> function does not retrieve the path for modules  that were loaded using the <b>LOAD_LIBRARY_AS_DATAFILE</b> flag. For more information, see <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>.


### -param hModule [in, optional]

A handle to the module. If this parameter is NULL, <b>GetModuleFileNameEx</b> returns the path of the executable file of the process specified in <i>hProcess</i>.


### -param lpFilename [out]

A pointer to a buffer that receives the fully qualified path to the module. If the size of the file name is larger than the value of the <i>nSize</i> parameter, the function succeeds but the file name is truncated and null-terminated.


### -param nSize [in]

The size of the <i>lpFilename</i> buffer, in characters.


## -returns



If the function succeeds, the return value specifies the length of the string copied to the buffer.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>GetModuleFileNameEx</b> function is primarily designed for use by debuggers and similar applications that must extract module information from another process. If the module list in the target process is corrupted or is not yet initialized, or if the module list changes during the function call as a result of DLLs being loaded or unloaded, <b>GetModuleFileNameEx</b> may fail or return incorrect information.

To retrieve the name of a module in the current process, use the <a href="https://msdn.microsoft.com/f124c99f-8be1-4a9c-a84c-b1b323921f1a">GetModuleFileName</a> function. This is more efficient and more reliable than calling <b>GetModuleFileNameEx</b> with a handle to the current process.

To retrieve the name of the main executable module for a remote process, use the <a href="https://msdn.microsoft.com/819fc2f4-0801-417b-9cbb-d7fd2894634e">GetProcessImageFileName</a> or <a href="https://msdn.microsoft.com/49a9d1aa-30f3-45ea-a4ec-9f55df692b8b">QueryFullProcessImageName</a> function. This is more efficient and more reliable than calling the <b>GetModuleFileNameEx</b> function with a NULL module handle.

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32GetModuleFileNameEx</b> in Psapi.h and exported in 
    Kernel32.lib and Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this 
    function is defined as <b>GetModuleFileNameEx</b> in 
    Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32GetModuleFileNameEx</b>. 

Programs that must run on earlier versions of Windows as 
    well as Windows 7 and later versions should always call this function as 
    <b>GetModuleFileNameEx</b>. To ensure correct resolution of symbols, 
    add Psapi.lib to the <b>TARGETLIBS</b> macro and compile the program with 
    <b>-DPSAPI_VERSION=1</b>. To use run-time dynamic linking, load Psapi.dll.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/2e411eba-ba60-4678-bf6f-bc15b6e8b478">Enumerating All Modules for a Process</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0c0445cb-27d2-4857-a4a5-7a4c180b068b">EnumProcesses</a>



<a href="https://msdn.microsoft.com/31a9eb69-95f0-4dd7-8fd5-296f2cff0b8a">GetModuleBaseName</a>



<a href="https://msdn.microsoft.com/f124c99f-8be1-4a9c-a84c-b1b323921f1a">GetModuleFileName</a>



<a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>



<a href="https://msdn.microsoft.com/e15b5e15-ca06-4733-bd0a-705058ba2db8">Module Information</a>



<a href="https://msdn.microsoft.com/e158792b-fec2-498d-aae3-d5679fa55783">PSAPI Functions</a>
 

 

