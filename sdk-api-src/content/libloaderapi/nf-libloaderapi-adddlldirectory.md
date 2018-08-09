---
UID: NF:libloaderapi.AddDllDirectory
title: AddDllDirectory function
author: windows-sdk-content
description: Adds a directory to the process DLL search path.
old-location: base\adddlldirectory.htm
old-project: dlls
ms.assetid: 7eb49bdf-58f9-4520-876b-c8b69bf26b8a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AddDllDirectory, AddDllDirectory function, base.adddlldirectory, libloaderapi/AddDllDirectory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: L2_NOTIFICATION_DATA, *PL2_NOTIFICATION_DATA
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
 - MinKernelBase.dll
 - API-MS-Win-Core-Libraryloader-l1-2-1.dll
 - API-MS-Win-Core-LibraryLoader-L1-2-2.dll
api_name:
 - AddDllDirectory
product: Windows
targetos: Windows
req.lib: 
req.dll: Kernel32.dll
req.irql: 
req.product: GDI+ 1.1
---

# AddDllDirectory function


## -description


Adds a directory to the process DLL search path.


## -parameters




### -param NewDirectory [in]

An absolute path to the directory to add to the search path. For example, to add the directory 
      Dir2 to the process DLL search path, specify \Dir2. For more information about paths, 
      see <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a>.


## -returns



If the function succeeds, the return value is an opaque pointer that can be passed to 
      <a href="https://msdn.microsoft.com/89ab63be-f0db-4f0f-9792-6976d867524e">RemoveDllDirectory</a> to remove the DLL from the 
      process DLL search path.

If the function fails, the return value is zero. To get extended error 
      information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>AddDllDirectory</b> function can be used to add 
    any absolute path to the set of directories that are searched for a DLL. If 
    <a href="https://msdn.microsoft.com/66884797-b1c8-4e50-aef1-e88944766d50">SetDefaultDllDirectories</a> is first called with 
    <b>LOAD_LIBRARY_SEARCH_USER_DIRS</b>, directories specified with 
    <b>AddDllDirectory</b> are added to the process DLL search 
    path. Otherwise, directories specified with the 
    <b>AddDllDirectory</b> function are used only for 
    <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a> function calls that specify 
    <b>LOAD_LIBRARY_SEARCH_USER_DIRS</b>.

If <b>AddDllDirectory</b> is used to add more than one 
    directory to the process DLL search path, the order in which those directories are searched is unspecified.

To remove a directory added with <b>AddDllDirectory</b>, 
    use the <a href="https://msdn.microsoft.com/89ab63be-f0db-4f0f-9792-6976d867524e">RemoveDllDirectory</a> function.

<b>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:  </b>To use this function in an application, call 
      <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to retrieve the function's address 
      from Kernel32.dll. 
      <a href="http://go.microsoft.com/fwlink/p/?linkid=217865">KB2533623</a> must be 
      installed on the target platform.



