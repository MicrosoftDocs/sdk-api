---
UID: NF:psapi.GetPerformanceInfo
title: GetPerformanceInfo function (psapi.h)
description: Retrieves the performance values contained in the PERFORMANCE_INFORMATION structure.
helpviewer_keywords: ["GetPerformanceInfo","GetPerformanceInfo function [PSAPI]","K32GetPerformanceInfo","_win32_getperformanceinfo","base.getperformanceinfo","psapi.getperformanceinfo","psapi/GetPerformanceInfo","psapi/K32GetPerformanceInfo"]
old-location: psapi\getperformanceinfo.htm
tech.root: psapi
ms.assetid: 21655278-49da-4e63-a4f9-0ee9f6179f4a
ms.date: 12/05/2018
ms.keywords: GetPerformanceInfo, GetPerformanceInfo function [PSAPI], K32GetPerformanceInfo, _win32_getperformanceinfo, base.getperformanceinfo, psapi.getperformanceinfo, psapi/GetPerformanceInfo, psapi/K32GetPerformanceInfo
req.header: psapi.h
req.include-header: 
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
req.lib: Kernel32.lib on Windows 7 and Windows Server 2008 R2; Psapi.lib (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.lib on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.dll: Kernel32.dll on Windows 7 and Windows Server 2008 R2; Psapi.dll (if PSAPI_VERSION=1) on Windows 7 and Windows Server 2008 R2; Psapi.dll on Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetPerformanceInfo
 - psapi/GetPerformanceInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - Psapi.dll
 - Psapi.dll
 - API-MS-Win-Core-PsAPI-L1-1-0.dll
 - KernelBase.dll
api_name:
 - GetPerformanceInfo
 - K32GetPerformanceInfo
---

# GetPerformanceInfo function


## -description

Retrieves the performance values contained in the 
    <a href="/windows/desktop/api/psapi/ns-psapi-performance_information">PERFORMANCE_INFORMATION</a> 
    structure.

## -parameters

### -param pPerformanceInformation [out]

A pointer to a 
      <a href="/windows/desktop/api/psapi/ns-psapi-performance_information">PERFORMANCE_INFORMATION</a> 
      structure that receives the performance information.

### -param cb [in]

The size of the 
      <a href="/windows/desktop/api/psapi/ns-psapi-performance_information">PERFORMANCE_INFORMATION</a> structure, in 
      bytes.

## -returns

If the function succeeds, the return value is TRUE. If the function fails, the return value is FALSE. To get 
       extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Starting with Windows 7 and Windows Server 2008 R2, Psapi.h establishes version numbers for 
    the PSAPI functions. The PSAPI version number affects the name used to call the function and the library that a 
    program must load.

If PSAPI_VERSION is 2 or greater, this function is defined as 
    <b>K32GetPerformanceInfo</b> in Psapi.h and exported in Kernel32.lib and Kernel32.dll. If 
    PSAPI_VERSION is 1, this function is defined as 
    <b>GetPerformanceInfo</b> in Psapi.h and exported in 
    Psapi.lib and Psapi.dll as a wrapper that calls <b>K32GetPerformanceInfo</b>.

Programs that must run on earlier versions of Windows as well as Windows 7 and later versions 
    should always call this function as 
    <b>GetPerformanceInfo</b>. To ensure correct resolution 
    of symbols, add Psapi.lib to the TARGETLIBS macro and compile the program with 
    –DPSAPI_VERSION=1. To use run-time dynamic linking, load Psapi.dll.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa965225(v=vs.85)">Memory Performance Information</a>



<a href="/windows/desktop/api/psapi/ns-psapi-performance_information">PERFORMANCE_INFORMATION</a>



<a href="/windows/desktop/psapi/psapi-functions">PSAPI Functions</a>