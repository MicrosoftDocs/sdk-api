---
UID: NC:shlwapi.DLLGETVERSIONPROC
title: DLLGETVERSIONPROC
author: windows-sdk-content
description: Implemented by many of the Windows Shell DLLs to allow applications to obtain DLL-specific version information.
old-location: shell\DllGetVersion.htm
old-project: shell
ms.assetid: d7ec0f7d-ba2f-4aa4-b867-a2615244a580
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: DLLGETVERSIONPROC, DLLGETVERSIONPROC callback, DllGetVersion, DllGetVersion callback function [Windows Shell], _win32_DllGetVersion, _win32_DllGetVersion_cpp, shell.DllGetVersion, shlwapi/DllGetVersion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: WALLPAPEROPT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Shlwapi.h
api_name:
 - DllGetVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# DLLGETVERSIONPROC callback function


## -description


Implemented by many of the Windows Shell DLLs to allow applications to obtain DLL-specific version information.


## -parameters




### -param *








#### - pdvi

Type: <b><a href="https://msdn.microsoft.com/bc6d856c-027f-43df-9bbc-a76f560dddb0">DLLVERSIONINFO</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/bc6d856c-027f-43df-9bbc-a76f560dddb0">DLLVERSIONINFO</a> structure that receives the version information. The <b>cbSize</b> member must be filled in before you call this function.


<a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Version 5.0</a>. DLLs that are shipped with Windows 2000 or later systems may return a <a href="https://msdn.microsoft.com/1648924d-0727-4cee-80d3-f97550f235cd">DLLVERSIONINFO2</a> structure. To maintain backward compatibility, the first member of a <b>DLLVERSIONINFO2</b> structure is a <a href="https://msdn.microsoft.com/bc6d856c-027f-43df-9bbc-a76f560dddb0">DLLVERSIONINFO</a> structure.


## -returns



Type: <b>HRESULT</b>

If this callback function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is exported by name from each DLL that implements it. Currently, most of the Windows Shell and controls DLLs implement <b>DllGetVersion</b>. These include, but are not limited to, Shell32.dll, Comctl32.dll, Shdocvw.dll, and Shlwapi.dll.

To call this function, use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to obtain the function pointer. The DLLGETVERSIONPROC type is used as the data type to define a pointer to a <b>DllGetVersion</b> function. Use the pointer when calling the function dynamically by loading the library and getting the function's address. See <a href="https://msdn.microsoft.com/ecfb6484-a1d6-4ace-8457-3940b111a4d2">Shell and Shlwapi DLL Versions</a> for a detailed discussion of the different file versions, and how to use <b>DllGetVersion</b>.



