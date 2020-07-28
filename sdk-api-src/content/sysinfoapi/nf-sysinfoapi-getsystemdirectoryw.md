---
UID: NF:sysinfoapi.GetSystemDirectoryW
title: GetSystemDirectoryW function (sysinfoapi.h)
description: Retrieves the path of the system directory.
helpviewer_keywords: ["GetSystemDirectory","GetSystemDirectory function","GetSystemDirectoryA","GetSystemDirectoryW","_win32_getsystemdirectory","base.getsystemdirectory","sysinfoapi/GetSystemDirectory","sysinfoapi/GetSystemDirectoryA","sysinfoapi/GetSystemDirectoryW"]
old-location: base\getsystemdirectory.htm
tech.root: winprog
ms.assetid: 79f045b2-40d9-498a-b720-e729c92bf50b
ms.date: 12/05/2018
ms.keywords: GetSystemDirectory, GetSystemDirectory function, GetSystemDirectoryA, GetSystemDirectoryW, _win32_getsystemdirectory, base.getsystemdirectory, sysinfoapi/GetSystemDirectory, sysinfoapi/GetSystemDirectoryA, sysinfoapi/GetSystemDirectoryW
f1_keywords:
- sysinfoapi/GetSystemDirectory
dev_langs:
- c++
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetSystemDirectoryW (Unicode) and GetSystemDirectoryA (ANSI)
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
- API-MS-Win-Core-SysInfo-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-SysInfo-l1-2-0.dll
- API-MS-Win-Core-SysInfo-l1-2-1.dll
- API-MS-Win-Core-SysInfo-l1-2-2.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
- API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
- GetSystemDirectory
- GetSystemDirectoryA
- GetSystemDirectoryW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetSystemDirectoryW function


## -description


Retrieves the path of the system directory. The system directory contains system files such as dynamic-link libraries and drivers.

This function is provided primarily for compatibility. Applications should store code in the Program Files folder and persistent data in the Application Data folder in the user's profile. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha">ShGetFolderPath</a>.


## -parameters




### -param lpBuffer [out]

A pointer to the buffer to receive the path. This path does not end with a backslash unless the system directory is the root directory. For example, if the system directory is named Windows\System32 on drive C, the path of the system directory retrieved by this function is C:\Windows\System32.


### -param uSize [in]

The maximum size of the buffer, in <b>TCHARs</b>.


## -returns



If the function succeeds, the return value is the length, in <b>TCHARs</b>, of the string copied to the buffer, not including the terminating null character. If the length is greater than the size of the buffer, the return value is the size of the buffer required to hold the path, including the terminating null character.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Applications should not create files in the system directory. If the user is running a shared version of the operating system, the application does not have write access to the system directory.


#### Examples

For an example, see 
<a href="https://docs.microsoft.com/windows/desktop/SysInfo/getting-system-information">Getting System Information</a>.

<div class="code"></div>




> [!NOTE]
> The sysinfoapi.h header defines GetSystemDirectory as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory">GetCurrentDirectory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya">GetWindowsDirectory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-setcurrentdirectory">SetCurrentDirectory</a>



<a href="https://docs.microsoft.com/windows/desktop/SysInfo/system-information-functions">System
		  Information Functions</a>
 

 

