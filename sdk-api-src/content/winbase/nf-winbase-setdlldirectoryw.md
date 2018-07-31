---
UID: NF:winbase.SetDllDirectoryW
title: SetDllDirectoryW function
author: windows-sdk-content
description: Adds a directory to the search path used to locate DLLs for the application.
old-location: base\setdlldirectory.htm
old-project: Dlls
ms.assetid: c0c57554-3d98-487c-8bae-c594620d5a00
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: SetDllDirectory, SetDllDirectory function, SetDllDirectoryA, SetDllDirectoryW, base.setdlldirectory, winbase/SetDllDirectory, winbase/SetDllDirectoryA, winbase/SetDllDirectoryW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetDllDirectoryW (Unicode) and SetDllDirectoryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - SetDllDirectory
 - SetDllDirectoryA
 - SetDllDirectoryW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetDllDirectoryW function


## -description


Adds a directory to the search path used to locate DLLs for the application.


## -parameters




### -param lpPathName [in, optional]

The directory to be added to the search path. If this parameter is an empty string (""), the call removes the current directory from the default DLL search order. If this parameter is NULL, the function restores the default search order.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>SetDllDirectory</b> function affects all subsequent calls to the 
<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and 
<a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a> functions. It also effectively disables safe DLL search mode while the specified directory is in the search path. 

After calling 
<b>SetDllDirectory</b>, the standard DLL search path is:

<ol>
<li>The directory from which the application loaded.</li>
<li>The directory specified by the <i>lpPathName</i> parameter.</li>
<li>The system directory. Use the 
<a href="https://msdn.microsoft.com/79f045b2-40d9-498a-b720-e729c92bf50b">GetSystemDirectory</a> function to get the path of this directory. The name of this directory is System32.</li>
<li>The 16-bit system directory. There is no function that obtains the path of this directory, but it is searched. The name of this directory is System.</li>
<li>The Windows directory. Use the 
<a href="https://msdn.microsoft.com/8c9b55e1-121a-4405-9f83-043752dd48ed">GetWindowsDirectory</a> function to get the path of this directory.</li>
<li>The directories that are listed in the PATH environment variable.</li>
</ol>
Each time the <b>SetDllDirectory</b> function is called, it replaces the directory specified in the previous <b>SetDllDirectory</b> call. To specify more than one directory, use the <a href="https://msdn.microsoft.com/7eb49bdf-58f9-4520-876b-c8b69bf26b8a">AddDllDirectory</a> function and call <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a> with LOAD_LIBRARY_SEARCH_USER_DIRS.

To revert to the standard search path used by 
<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and 
<a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>, call 
<b>SetDllDirectory</b> with NULL. This also restores safe DLL search mode  based on the <b>SafeDllSearchMode</b> registry value.

To compile an application that uses this function, define _WIN32_WINNT as 0x0502 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/7eb49bdf-58f9-4520-876b-c8b69bf26b8a">AddDllDirectory</a>



<a href="https://msdn.microsoft.com/44228cf2-6306-466c-8f16-f513cd3ba8b5">Dynamic-Link Library Search Order</a>



<a href="https://msdn.microsoft.com/f892546a-6c48-48f2-8d9a-46e448fffb89">GetDllDirectory</a>



<a href="https://msdn.microsoft.com/79f045b2-40d9-498a-b720-e729c92bf50b">GetSystemDirectory</a>



<a href="https://msdn.microsoft.com/8c9b55e1-121a-4405-9f83-043752dd48ed">GetWindowsDirectory</a>



<a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a>



<a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>
 

 

