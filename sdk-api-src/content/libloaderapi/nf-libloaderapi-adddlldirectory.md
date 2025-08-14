---
UID: NF:libloaderapi.AddDllDirectory
title: AddDllDirectory function (libloaderapi.h)
description: Adds a directory to the process DLL search path.
helpviewer_keywords: ["AddDllDirectory","AddDllDirectory function","base.adddlldirectory","libloaderapi/AddDllDirectory"]
old-location: base\adddlldirectory.htm
tech.root: base
ms.assetid: 7eb49bdf-58f9-4520-876b-c8b69bf26b8a
ms.date: 12/05/2018
ms.keywords: AddDllDirectory, AddDllDirectory function, base.adddlldirectory, libloaderapi/AddDllDirectory
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only],KB2533623      on Windows 7, Windows Server 2008 R2, Windows Vista, and      Windows Server 2008
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AddDllDirectory
 - libloaderapi/AddDllDirectory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-libraryloader-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-LibraryLoader-l1-1-1.dll
 - API-MS-Win-Core-LibraryLoader-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-Libraryloader-l1-2-1.dll
 - API-MS-Win-Core-LibraryLoader-L1-2-2.dll
api_name:
 - AddDllDirectory
---

# AddDllDirectory function


## -description

Adds a directory to the process DLL search path.

## -parameters

### -param NewDirectory [in]

An absolute path to the directory to add to the search path. For example, to add the directory 
      Dir2 to the process DLL search path, specify \Dir2. For more information about paths, 
      see <a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a>.

## -returns

If the function succeeds, the return value is an opaque pointer that can be passed to 
      <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-removedlldirectory">RemoveDllDirectory</a> to remove the DLL from the 
      process DLL search path.

If the function fails, the return value is zero. To get extended error 
      information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>AddDllDirectory</b> function can be used to add 
    any absolute path to the set of directories that are searched for a DLL. If 
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-setdefaultdlldirectories">SetDefaultDllDirectories</a> is first called with 
    <b>LOAD_LIBRARY_SEARCH_USER_DIRS</b>, directories specified with 
    <b>AddDllDirectory</b> are added to the process DLL search 
    path. Otherwise, directories specified with the 
    <b>AddDllDirectory</b> function are used only for 
    <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibraryexa">LoadLibraryEx</a> function calls that specify 
    <b>LOAD_LIBRARY_SEARCH_USER_DIRS</b>.

If <b>AddDllDirectory</b> is used to add more than one 
    directory to the process DLL search path, the order in which those directories are searched is unspecified.

To remove a directory added with <b>AddDllDirectory</b>, 
    use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-removedlldirectory">RemoveDllDirectory</a> function.

<b>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:  </b>To use this function in an application, call 
      <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to retrieve the function's address 
      from Kernel32.dll. 
      <a href="https://support.microsoft.com/kb/2533623">KB2533623</a> must be 
      installed on the target platform.