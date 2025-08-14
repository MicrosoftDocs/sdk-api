---
UID: NF:sysinfoapi.GetSystemWindowsDirectoryA
title: GetSystemWindowsDirectoryA function (sysinfoapi.h)
description: Retrieves the path of the shared Windows directory on a multi-user system. (ANSI)
helpviewer_keywords: ["GetSystemWindowsDirectoryA", "sysinfoapi/GetSystemWindowsDirectoryA"]
old-location: base\getsystemwindowsdirectory.htm
tech.root: winprog
ms.assetid: 4f0955fb-8fa3-4102-b2a5-44ce5cbd2e35
ms.date: 12/05/2018
ms.keywords: GetSystemWindowsDirectory, GetSystemWindowsDirectory function, GetSystemWindowsDirectoryA, GetSystemWindowsDirectoryW, _win32_getsystemwindowsdirectory, base.getsystemwindowsdirectory, sysinfoapi/GetSystemWindowsDirectory, sysinfoapi/GetSystemWindowsDirectoryA, sysinfoapi/GetSystemWindowsDirectoryW
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetSystemWindowsDirectoryW (Unicode) and GetSystemWindowsDirectoryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetSystemWindowsDirectoryA
 - sysinfoapi/GetSystemWindowsDirectoryA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-sysinfo-l1-2-7.dll
 - api-ms-win-core-sysinfo-l1-2-6.dll
 - api-ms-win-core-sysinfo-l1-2-5.dll
 - api-ms-win-core-sysinfo-l1-2-4.dll
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
 - GetSystemWindowsDirectory
 - GetSystemWindowsDirectoryA
 - GetSystemWindowsDirectoryW
---

# GetSystemWindowsDirectoryA function


## -description

Retrieves the path of the shared Windows directory on a multi-user system.

This function is provided primarily for compatibility. Applications should store code in the Program Files folder and persistent data in the Application Data folder in the user's profile. For more information, see 
<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha">ShGetFolderPath</a>.

## -parameters

### -param lpBuffer [out]

A pointer to the buffer to receive the path. This path does not end with a backslash unless the Windows directory is the root directory. For example, if the Windows directory is named Windows on drive C, the path of the Windows directory retrieved by this function is C:\Windows. If the system was installed in the root directory of drive C, the path retrieved is C:\.

### -param uSize [in]

The maximum size of the buffer specified by the <i>lpBuffer</i> parameter, in <b>TCHARs</b>.

## -returns

If the function succeeds, the return value is the length of the string copied to the buffer, in <b>TCHARs</b>, not including the terminating null character.

If the length is greater than the size of the buffer, the return value is the size of the buffer required to hold the path.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

On a system that is running Terminal Services, each user has a unique Windows directory. The system Windows directory is shared by all users, so it is the directory where an application should store initialization and help files that apply to all users.

With Terminal Services, the 
<b>GetSystemWindowsDirectory</b> function retrieves the path of the system Windows directory, while the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya">GetWindowsDirectory</a> function retrieves the path of a Windows directory that is private for each user. On a single-user system, 
<b>GetSystemWindowsDirectory</b> is the same as 
<b>GetWindowsDirectory</b>.





> [!NOTE]
> The sysinfoapi.h header defines GetSystemWindowsDirectory as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya">GetWindowsDirectory</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation">SHGetFolderLocation</a>



<a href="/windows/desktop/SysInfo/system-information-functions">System
		  Information Functions</a>
