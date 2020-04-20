---
UID: NF:wow64apiset.IsWow64Process
title: IsWow64Process function (wow64apiset.h)
description: Determines whether the specified process is running under WOW64 or an Intel64 of x64 processor.helpviewer_keywords: ["IsWow64Process","IsWow64Process function","_win32_iswow64process","base.iswow64process","winbase/IsWow64Process","wow64apiset/IsWow64Process"]
old-location: base\iswow64process.htm
tech.root: ProcThread
ms.assetid: 5a237542-e432-487c-aa59-2ede427dd1eb
ms.date: 12/05/2018
ms.keywords: IsWow64Process, IsWow64Process function, _win32_iswow64process, base.iswow64process, winbase/IsWow64Process, wow64apiset/IsWow64Process
f1_keywords:
- wow64apiset/IsWow64Process
dev_langs:
- c++
req.header: wow64apiset.h
req.include-header: Windows Server 2003, Windows Vista, Windows 7, Windows Server 2008  Windows Server 2008 R2, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps \| UWP apps]
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
- API-MS-Win-Core-misc-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-Wow64-l1-1-0.dll
- API-MS-Win-Core-Wow64-l1-1-1.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
- bcrypt.dll
api_name:
- IsWow64Process
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IsWow64Process function


## -description


Determines whether the specified process is running under 
<a href="https://docs.microsoft.com/windows/desktop/WinProg64/running-32-bit-applications">WOW64</a> or an Intel64 of x64 processor.


## -parameters




### -param hProcess [in]

A handle to the process. The handle must have the PROCESS_QUERY_INFORMATION or PROCESS_QUERY_LIMITED_INFORMATION access right. For more information, see <a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the PROCESS_QUERY_INFORMATION access right.


### -param Wow64Process [out]

A pointer to a value that is set to TRUE if the process is running under WOW64 on an Intel64 or x64 processor. If the process is running under 32-bit Windows, the value is set to FALSE. If the process is a 32-bit application running under 64-bit Windows 10 on ARM, the value is set to FALSE. If the process is a 64-bit application running under 64-bit Windows, the value is also set to FALSE. 


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Applications should use <a href="https://docs.microsoft.com/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process2">IsWow64Process2</a> instead of <b>IsWow64Process</b> to determine if a process is running under WOW.  <b>IsWow64Process2</b> removes the ambiguity inherent to multiple WOW environments by explicitly returning both the architecture of the host and guest for a given process.  Applications can use this information to reliably identify situations such as running under emulation on ARM64. To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples

For compatibility with operating systems that do not support this function, call 
<a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to detect whether 
<b>IsWow64Process</b> is implemented in Kernel32.dll. If <b>GetProcAddress</b> succeeds, it is safe to call this function. Otherwise, WOW64 is not present. Note that this technique is not a reliable way to detect whether the operating system is a 64-bit version of Windows because the Kernel32.dll in current versions of 32-bit Windows also contains this function.


```cpp
#include <windows.h>
#include <tchar.h>

typedef BOOL (WINAPI *LPFN_ISWOW64PROCESS) (HANDLE, PBOOL);

LPFN_ISWOW64PROCESS fnIsWow64Process;

BOOL IsWow64()
{
    BOOL bIsWow64 = FALSE;

    //IsWow64Process is not available on all supported versions of Windows.
    //Use GetModuleHandle to get a handle to the DLL that contains the function
    //and GetProcAddress to get a pointer to the function if available.

    fnIsWow64Process = (LPFN_ISWOW64PROCESS) GetProcAddress(
        GetModuleHandle(TEXT("kernel32")),"IsWow64Process");

    if(NULL != fnIsWow64Process)
    {
        if (!fnIsWow64Process(GetCurrentProcess(),&bIsWow64))
        {
            //handle error
        }
    }
    return bIsWow64;
}

int main( void )
{
    if(IsWow64())
        _tprintf(TEXT("The process is running under WOW64.\n"));
    else
        _tprintf(TEXT("The process is not running under WOW64.\n"));

    return 0;
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo">GetNativeSystemInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-iswow64message">IsWow64Message</a>



<a href="https://docs.microsoft.com/windows/desktop/WinProg64/running-32-bit-applications">WOW64</a>
 

 

