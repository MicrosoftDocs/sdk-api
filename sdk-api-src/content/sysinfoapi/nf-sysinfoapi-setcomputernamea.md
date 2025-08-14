---
UID: NF:sysinfoapi.SetComputerNameA
title: SetComputerNameA function (sysinfoapi.h)
description: Sets a new NetBIOS name for the local computer. The name is stored in the registry and the name change takes effect the next time the user restarts the computer. (ANSI)
helpviewer_keywords: ["SetComputerNameA", "sysinfoapi/SetComputerNameA"]
old-location: base\setcomputername.htm
tech.root: winprog
ms.assetid: ff64fde2-d1b5-4211-b8c4-4823a5469e04
ms.date: 12/05/2018
ms.keywords: SetComputerName, SetComputerName function, SetComputerNameA, SetComputerNameW, _win32_setcomputername, base.setcomputername, sysinfoapi/SetComputerName, sysinfoapi/SetComputerNameA, sysinfoapi/SetComputerNameW
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetComputerNameW (Unicode) and SetComputerNameA (ANSI)
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
 - SetComputerNameA
 - sysinfoapi/SetComputerNameA
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
 - API-Ms-Win-Core-SysInfo-L1-2-3.dll
 - KernelBase.dll
api_name:
 - SetComputerName
 - SetComputerNameA
 - SetComputerNameW
---

# SetComputerNameA function


## -description

Sets a new NetBIOS name for the local computer. The name is stored in the registry and the name change takes effect the next time the user restarts the computer.

If the local computer is a node in a cluster, 
<b>SetComputerName</b> sets NetBIOS name of the local computer, not that of the cluster virtual server.

To set the DNS host name or the DNS domain name, call the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa">SetComputerNameEx</a> function.

## -parameters

### -param lpComputerName [in]

The computer name that will take effect the next time the computer is started. The name must not be longer than MAX_COMPUTERNAME_LENGTH characters. 




The standard character set includes letters, numbers, and the following symbols: ! @ # $ % ^ &amp; ' ) ( . - _ { } ~ . If this parameter contains one or more characters that are outside the standard character set, 
<b>SetComputerName</b> returns ERROR_INVALID_PARAMETER.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Applications using this function must have administrator rights.





> [!NOTE]
> The sysinfoapi.h header defines SetComputerName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SysInfo/computer-names">Computer Names</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getcomputernamea">GetComputerName</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa">GetComputerNameEx</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa">SetComputerNameEx</a>



<a href="/windows/desktop/SysInfo/system-information-functions">System Information Functions</a>
