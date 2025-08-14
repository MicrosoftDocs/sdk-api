---
UID: NF:libloaderapi.RemoveDllDirectory
title: RemoveDllDirectory function (libloaderapi.h)
description: Removes a directory that was added to the process DLL search path by using AddDllDirectory.
helpviewer_keywords: ["RemoveDllDirectory","RemoveDllDirectory function","base.removedlldirectory","libloaderapi/RemoveDllDirectory"]
old-location: base\removedlldirectory.htm
tech.root: base
ms.assetid: 89ab63be-f0db-4f0f-9792-6976d867524e
ms.date: 12/05/2018
ms.keywords: RemoveDllDirectory, RemoveDllDirectory function, base.removedlldirectory, libloaderapi/RemoveDllDirectory
req.header: libloaderapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only],KB2533623     on Windows 7, Windows Server 2008 R2, Windows Vista, and     Windows Server 2008
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
 - RemoveDllDirectory
 - libloaderapi/RemoveDllDirectory
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
 - RemoveDllDirectory
---

# RemoveDllDirectory function


## -description

Removes a directory that was added to the process DLL search path by using 
     <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-adddlldirectory">AddDllDirectory</a>.

## -parameters

### -param Cookie [in]

The cookie returned by <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-adddlldirectory">AddDllDirectory</a> when the 
      directory was added to the search path.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value 
      is zero. To get extended error information, call 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

After <b>RemoveDllDirectory</b> returns, the cookie is 
    no longer valid and should not be used.

<b>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:  </b>To call this function in an application, use the 
      <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> function to retrieve its address from 
      Kernel32.dll. 
      <a href="https://support.microsoft.com/kb/2533623">KB2533623</a> must be 
      installed on the target platform.