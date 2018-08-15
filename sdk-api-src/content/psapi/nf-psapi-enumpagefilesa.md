---
UID: NF:psapi.EnumPageFilesA
title: EnumPageFilesA function
author: windows-sdk-content
description: Calls the callback routine for each installed pagefile in the system.
old-location: psapi\enumpagefiles.htm
old-project: psapi
ms.assetid: 9289fe3c-a7d9-4acb-aeb6-a50de65db0a2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EnumPageFiles, EnumPageFiles function [PSAPI], EnumPageFilesA, EnumPageFilesW, K32EnumPageFiles, K32EnumPageFilesA, K32EnumPageFilesW, _win32_enumpagefiles, base.enumpagefiles, psapi.enumpagefiles, psapi/EnumPageFiles, psapi/EnumPageFilesA, psapi/EnumPageFilesW, psapi/K32EnumPageFiles, psapi/K32EnumPageFilesA, psapi/K32EnumPageFilesW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: psapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: EnumPageFilesW (Unicode) and EnumPageFilesA (ANSI)
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
 - API-MS-Win-Core-PsAPI-Ansi-L1-1-0.dll
 - API-MS-Win-Core-PsAPI-L1-1-0.dll
 - KernelBase.dll
api_name:
 - EnumPageFiles
 - EnumPageFilesA
 - EnumPageFilesW
 - K32EnumPageFiles
 - K32EnumPageFilesW
 - K32EnumPageFilesA
product: Windows
targetos: Windows
req.lib: Kernel32.lib on Windows 7 and Windows Server 2008 R2; Psapi.lib (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.lib on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.dll: Kernel32.dll on Windows 7 and Windows Server 2008 R2; Psapi.dll (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.irql: 
req.product: ADAM
---

# EnumPageFilesA function


## -description


Calls the callback routine for each installed pagefile in the system.


## -parameters




### -param pCallBackRoutine [out]

A pointer to the routine called for each pagefile. For more information, see 
      <a href="https://msdn.microsoft.com/eb3610fb-2c95-4f7b-973d-8dc41d2829f1">EnumPageFilesProc</a>.


### -param pContext [in]

The user-defined data passed to the callback routine.


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the 
       return value is <b>FALSE</b>. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes 
    version numbers for the PSAPI functions. The PSAPI version number affects  the name used to call the function and 
    the library that a program must load.

If <b>PSAPI_VERSION</b> is 2 or greater, this function is defined as 
    <b>K32EnumPageFiles</b> in Psapi.h and exported in Kernel32.lib and 
    Kernel32.dll. If <b>PSAPI_VERSION</b> is 1, this function is defined as 
    <b>EnumPageFiles</b> in Psapi.h and exported in 
    Psapi.lib and Psapi.dll as a wrapper that calls 
    <b>K32EnumPageFiles</b>.

Programs that must run on earlier versions of Windows as well as Windows 7 and later versions 
    should always call this function as <b>EnumPageFiles</b>. To 
    ensure correct resolution of symbols, add Psapi.lib to the <b>TARGETLIBS</b> 
    macro and compile the program with –DPSAPI_VERSION=1. To use run-time dynamic linking, load 
    Psapi.dll.




## -see-also




<a href="https://msdn.microsoft.com/eb3610fb-2c95-4f7b-973d-8dc41d2829f1">EnumPageFilesProc</a>



<a href="https://msdn.microsoft.com/e158792b-fec2-498d-aae3-d5679fa55783">PSAPI Functions</a>
 

 

