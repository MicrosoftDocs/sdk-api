---
UID: NF:sysinfoapi.GetWindowsDirectoryW
title: GetWindowsDirectoryW function (sysinfoapi.h)
description: Retrieves the path of the Windows directory. (Unicode)
helpviewer_keywords: ["GetWindowsDirectory", "GetWindowsDirectory function", "GetWindowsDirectoryW", "_win32_getwindowsdirectory", "base.getwindowsdirectory", "sysinfoapi/GetWindowsDirectory", "sysinfoapi/GetWindowsDirectoryW"]
old-location: base\getwindowsdirectory.htm
tech.root: winprog
ms.assetid: 8c9b55e1-121a-4405-9f83-043752dd48ed
ms.date: 12/05/2018
ms.keywords: GetWindowsDirectory, GetWindowsDirectory function, GetWindowsDirectoryA, GetWindowsDirectoryW, _win32_getwindowsdirectory, base.getwindowsdirectory, sysinfoapi/GetWindowsDirectory, sysinfoapi/GetWindowsDirectoryA, sysinfoapi/GetWindowsDirectoryW
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetWindowsDirectoryW (Unicode) and GetWindowsDirectoryA (ANSI)
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
 - GetWindowsDirectoryW
 - sysinfoapi/GetWindowsDirectoryW
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
 - GetWindowsDirectory
 - GetWindowsDirectoryA
 - GetWindowsDirectoryW
---

# GetWindowsDirectoryW function


## -description

Retrieves the 
    path of the Windows directory.

This function is provided primarily for compatibility with legacy applications. New applications should store code in the Program Files folder 
    and persistent data in the Application Data folder in the user's profile. For more information, see 
    <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha">ShGetFolderPath</a>.

## -parameters

### -param lpBuffer [out]

A pointer to a buffer that receives the path. This path does not end with a 
      backslash unless the Windows directory is the root directory. For example, if the Windows directory is named 
      Windows on drive C, the path of the Windows directory retrieved by this function is C:\Windows. If the system 
      was installed in the root directory of drive C, the path retrieved is C:\.

### -param uSize [in]

The maximum size of the buffer specified by the <i>lpBuffer</i> parameter, in 
      <b>TCHARs</b>. This value should be set to <b>MAX_PATH</b>.

## -returns

If the function succeeds, the return value is the length of the string copied to the buffer, in 
       <b>TCHARs</b>, not including the terminating null character.
      

If the length is greater than the size of the buffer, the return value is the size of the buffer required to 
       hold the path.
      

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The Windows directory is the directory where some legacy applications  store initialization and help files. New applications should not store files in the Windows directory; instead, they should store system-wide data in the application's installation directory, and user-specific data in the user's profile.

If the 
    user is running a shared version of the system, the Windows directory is guaranteed to be private for each user.
   

If an application creates other files that it wants to store on a per-user basis, it should place them in the 
    directory specified by the HOMEPATH environment variable. This directory will be different for each user, if so 
    specified by an administrator, through the User Manager administrative tool. HOMEPATH always specifies either the 
    user's home directory, which is guaranteed to be private for each user, or a default directory (for example, 
    C:\USERS\DEFAULT) where the user will have all access.
   

<b>Terminal Services:  </b>If the application is running in a Terminal Services environment, each user has a private Windows directory. 
     There is also a shared Windows directory for the system. If the application is Terminal-Services-aware (has the 
     <b>IMAGE_DLLCHARACTERISTICS_TERMINAL_SERVER_AWARE</b> flag set in the image header), this 
     function returns the path of the system Windows directory, just as the 
     <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemwindowsdirectorya">GetSystemWindowsDirectory</a> function does. 
     Otherwise, it retrieves the path of the private Windows directory for the user.


#### Examples

For an example, see <a href="/windows/desktop/SysInfo/getting-system-information">Getting System Information</a>.

<div class="code"></div>




> [!NOTE]
> The sysinfoapi.h header defines GetWindowsDirectory as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getcurrentdirectory">GetCurrentDirectory</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya">GetSystemDirectory</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemwindowsdirectorya">GetSystemWindowsDirectory</a>



<a href="/windows/desktop/SysInfo/system-information-functions">System Information Functions</a>
