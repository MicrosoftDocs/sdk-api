---
UID: NF:libloaderapi.SizeofResource
title: SizeofResource function (libloaderapi.h)
author: windows-sdk-content
description: Retrieves the size, in bytes, of the specified resource.
old-location: menurc\sizeofresource.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcefunctions\sizeofresource.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SizeofResource, SizeofResource function [Menus and Other Resources], _win32_SizeofResource, _win32_sizeofresource_cpp, libloaderapi/SizeofResource, menurc.sizeofresource, winui._win32_sizeofresource
ms.topic: function
f1_keywords: ["libloaderapi/SizeofResource"]
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
 - API-MS-Win-Core-LibraryLoader-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-1.dll
 - API-MS-Win-Core-LibraryLoader-l1-2-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Libraryloader-l1-2-1.dll
 - API-MS-Win-Core-LibraryLoader-L1-2-2.dll
api_name:
 - SizeofResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SizeofResource function


## -description


Retrieves the size, in bytes, of the specified resource.


## -parameters




### -param hModule [in, optional]

Type: <b>HMODULE</b>

A handle to the module whose executable file contains the resource.


### -param hResInfo [in]

Type: <b>HRSRC</b>

A handle to the resource. This handle must be created by using the <a href="https://msdn.microsoft.com/00f14551-5381-4499-a13a-86f15dd4e618">FindResource</a> or <a href="https://msdn.microsoft.com/3a9bfcca-68d8-4705-914b-dae844b5e0c3">FindResourceEx</a> function.


## -returns



Type: <b>DWORD</b>

If the function succeeds, the return value is the number of bytes in the resource.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/00f14551-5381-4499-a13a-86f15dd4e618">FindResource</a>



<a href="https://msdn.microsoft.com/3a9bfcca-68d8-4705-914b-dae844b5e0c3">FindResourceEx</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
 

 

