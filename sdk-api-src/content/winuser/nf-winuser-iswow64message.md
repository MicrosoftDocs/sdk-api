---
UID: NF:winuser.IsWow64Message
title: IsWow64Message function (winuser.h)
description: Determines whether the last message read from the current thread's queue originated from a WOW64 process.
helpviewer_keywords: ["IsWow64Message","IsWow64Message function","base.iswow64message","winuser/IsWow64Message"]
old-location: base\iswow64message.htm
tech.root: backup
ms.assetid: bc0ac424-3c5b-41bf-9dae-bcb405d5b548
ms.date: 12/05/2018
ms.keywords: IsWow64Message, IsWow64Message function, base.iswow64message, winuser/IsWow64Message
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IsWow64Message
 - winuser/IsWow64Message
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - IsWow64Message
---

# IsWow64Message function


## -description

Determines whether the last message read from the current thread's queue originated from a <a href="/windows/desktop/WinProg64/running-32-bit-applications">WOW64</a> process.



## -returns

The function returns TRUE if the last message read from the current thread's queue originated from a WOW64 process, and FALSE otherwise.

## -remarks

This function  is useful to helping you develop 64-bit native applications that can receive private messages sent from  32-bit client applications, if the messages are associated with data structures that contain pointer-dependent data. In these situations, you can call this function in your 64-bit native application to determine if the message originated from a WOW64 process and then thunk the message appropriately.


#### Examples

For compatibility with operating systems that do not support this function, call 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to detect whether 
<b>IsWow64Message</b> is implemented in User32.dll. If <b>GetProcAddress</b> succeeds, it is safe to call this function. Otherwise, WOW64 is not present. Note that this technique is not a reliable way to detect whether the operating system is a 64-bit version of Windows because the User32.dll in current versions of 32-bit Windows also contains this function.


```cpp
#include <windows.h>
#include <tchar.h>

typedef BOOL (WINAPI *LPFN_ISWOW64MESSAGE) (void);

LPFN_ISWOW64MESSAGE fnIsWow64Message;

BOOL IsWow64Msg()
{
    // IsWow64Message is not available on all supported versions of Windows
    // Use LoadLibrary to ensure that the DLL containing the function is loaded
    // and GetProcAddress to get a pointer to the function if available.

    fnIsWow64Message = (LPFN_ISWOW64MESSAGE) GetProcAddress(
        LoadLibrary(TEXT("user32")), "IsWow64Message");
  
    if (NULL != fnIsWow64Message)
    {        
        return (fnIsWow64Message());
    }
    else return FALSE;
}

int main( void )
{
    if(IsWow64Msg())
    {
        _tprintf(TEXT("The last message was from a 32-bit process.\n"));
    }
    else if (NULL == fnIsWow64Message )
    {
        _tprintf(TEXT("The IsWow64Message function is not available (%d).\n"), GetLastError());
    }
    else 
    {
        _tprintf(TEXT("The last message was from a 64-bit process.\n"));
    }
    return 0;
}

```

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo">GetNativeSystemInfo</a>



<a href="/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process">IsWow64Process</a>



<a href="/windows/desktop/WinProg64/running-32-bit-applications">WOW64</a>
