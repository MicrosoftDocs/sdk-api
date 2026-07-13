---
UID: NC:shlwapi.DLLGETVERSIONPROC
title: DLLGETVERSIONPROC (shlwapi.h)
description: Implemented by many of the Windows Shell DLLs to allow applications to obtain DLL-specific version information.
helpviewer_keywords: ["DLLGETVERSIONPROC","DLLGETVERSIONPROC callback","DllGetVersion","DllGetVersion callback function [Windows Shell]","_win32_DllGetVersion","_win32_DllGetVersion_cpp","shell.DllGetVersion","shlwapi/DllGetVersion"]
old-location: shell\DllGetVersion.htm
tech.root: shell
ms.assetid: d7ec0f7d-ba2f-4aa4-b867-a2615244a580
ms.date: 12/05/2018
ms.keywords: DLLGETVERSIONPROC, DLLGETVERSIONPROC callback, DllGetVersion, DllGetVersion callback function [Windows Shell], _win32_DllGetVersion, _win32_DllGetVersion_cpp, shell.DllGetVersion, shlwapi/DllGetVersion
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DLLGETVERSIONPROC
 - shlwapi/DLLGETVERSIONPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Shlwapi.h
api_name:
 - DllGetVersion
---

# DLLGETVERSIONPROC callback function


## -description

Implemented by many of the Windows Shell DLLs to allow applications to obtain DLL-specific version information.

## -parameters

### -param 

#### - pdvi

Type: <b><a href="/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo">DLLVERSIONINFO</a>*</b>

A pointer to a <a href="/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo">DLLVERSIONINFO</a> structure that receives the version information. The <b>cbSize</b> member must be filled in before you call this function.


<a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 5.0</a>. DLLs that are shipped with Windows 2000 or later systems may return a <a href="/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2">DLLVERSIONINFO2</a> structure. To maintain backward compatibility, the first member of a <b>DLLVERSIONINFO2</b> structure is a <a href="/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo">DLLVERSIONINFO</a> structure.

## -returns

Type: <b>HRESULT</b>

If this callback function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is exported by name from each DLL that implements it. Currently, most of the Windows Shell and controls DLLs implement <b>DllGetVersion</b>. These include, but are not limited to, Shell32.dll, Comctl32.dll, Shdocvw.dll, and Shlwapi.dll.

To call this function, use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions to obtain the function pointer. The DLLGETVERSIONPROC type is used as the data type to define a pointer to a <b>DllGetVersion</b> function. Use the pointer when calling the function dynamically by loading the library and getting the function's address. See <a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Shell and Shlwapi DLL Versions</a> for a detailed discussion of the different file versions, and how to use <b>DllGetVersion</b>.
