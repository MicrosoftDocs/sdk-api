---
UID: NF:psapi.GetModuleInformation
title: GetModuleInformation function
author: windows-sdk-content
description: Retrieves information about the specified module in the MODULEINFO structure.
old-location: psapi\getmoduleinformation.htm
old-project: psapi
ms.assetid: afb9f4c8-c8ae-4497-96c1-b559cfa2cedf
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetModuleInformation, GetModuleInformation function [PSAPI], K32GetModuleInformation, _win32_getmoduleinformation, base.getmoduleinformation, psapi.getmoduleinformation, psapi/GetModuleInformation, psapi/K32GetModuleInformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: psapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PSHNOTIFY, *LPPSHNOTIFY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	Psapi.dll
-	Psapi.dll
-	API-MS-Win-Core-PsAPI-Obsolete-L1-1-0.dll
-	KernelBase.dll
-	API-Ms-Win-Core-PsAPI-L1-1-0.dll
api_name:
-	GetModuleInformation
-	K32GetModuleInformation
product: Windows
targetos: Windows
req.lib: Kernel32.lib on Windows 7 and Windows Server 2008 R2; Psapi.lib (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.lib on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.dll: Kernel32.dll on Windows 7 and Windows Server 2008 R2; Psapi.dll (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# GetModuleInformation function


## -description


Retrieves information about the specified module in the 
<a href="https://msdn.microsoft.com/583caafe-7fa3-4041-b5bc-4e8899b3a08a">MODULEINFO</a> structure.


## -parameters




### -param hProcess [in]

A handle to the process that contains the module.

The handle must have the <b>PROCESS_QUERY_INFORMATION</b> and <b>PROCESS_VM_READ</b> access rights. For more information, see <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.


### -param hModule [in]

A handle to the module.


### -param lpmodinfo [out]

A pointer to the 
<a href="https://msdn.microsoft.com/583caafe-7fa3-4041-b5bc-4e8899b3a08a">MODULEINFO</a> structure that receives information about the module.


### -param cb [in]

The size of the 
<a href="https://msdn.microsoft.com/583caafe-7fa3-4041-b5bc-4e8899b3a08a">MODULEINFO</a> structure, in bytes.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To get information for the calling process, pass the handle returned by <a href="https://msdn.microsoft.com/0471790c-3bb9-4180-8676-941e655b1812">GetCurrentProcess</a>.

The <b>GetModuleInformation</b> function does not retrieve information for modules that were loaded with the <b>LOAD_LIBRARY_AS_DATAFILE</b> flag. For more information, see <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>.

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32GetModuleInformation</b> in Psapi.h and exported in 
    Kernel32.lib and Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this 
    function is defined as K32GetModuleInformation in 
    Psapi.h and exported in Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32GetModuleInformation</b>. 

Programs that must run on earlier versions of Windows as 
    well as Windows 7 and later versions should always call this function as 
    K32GetModuleInformation. To ensure correct resolution of symbols, 
    add Psapi.lib to the <b>TARGETLIBS</b> macro and compile the program with 
    <b>-DPSAPI_VERSION=1</b>. To use run-time dynamic linking, load Psapi.dll.




## -see-also




<a href="https://msdn.microsoft.com/0c0445cb-27d2-4857-a4a5-7a4c180b068b">EnumProcesses</a>



<a href="https://msdn.microsoft.com/583caafe-7fa3-4041-b5bc-4e8899b3a08a">MODULEINFO</a>



<a href="https://msdn.microsoft.com/e15b5e15-ca06-4733-bd0a-705058ba2db8">Module Information</a>



<a href="https://msdn.microsoft.com/e158792b-fec2-498d-aae3-d5679fa55783">PSAPI Functions</a>
 

 

