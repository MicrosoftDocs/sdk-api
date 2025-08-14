---
UID: NF:winbase.GetComputerNameA
title: GetComputerNameA function (winbase.h)
description: Retrieves the NetBIOS name of the local computer. This name is established at system startup, when the system reads it from the registry. (ANSI)
helpviewer_keywords: ["GetComputerNameA", "winbase/GetComputerNameA"]
old-location: base\getcomputername.htm
tech.root: winprog
ms.assetid: 8ca3e611-e5fb-4909-adf6-98eb8552c9e1
ms.date: 12/05/2018
ms.keywords: GetComputerName, GetComputerName function, GetComputerNameA, GetComputerNameW, _win32_getcomputername, base.getcomputername, winbase/GetComputerName, winbase/GetComputerNameA, winbase/GetComputerNameW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetComputerNameW (Unicode) and GetComputerNameA (ANSI)
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
 - GetComputerNameA
 - winbase/GetComputerNameA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetComputerName
 - GetComputerNameA
 - GetComputerNameW
---

# GetComputerNameA function


## -description

Retrieves the NetBIOS name of the local computer. This name is established at system startup, when the system reads it from the registry.

<b>GetComputerName</b> retrieves only the NetBIOS name of the local computer. To retrieve the DNS host name, DNS domain name, or the fully qualified DNS name, call the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa">GetComputerNameEx</a> function. Additional information is provided by the 
<a href="/windows/desktop/api/iads/nn-iads-iadsadsysteminfo">IADsADSystemInfo</a> interface.

The behavior of this function can be affected if the local computer is a node in a cluster. For more information, see <a href="/windows/desktop/api/resapi/nf-resapi-resutilgetenvironmentwithnetname">ResUtilGetEnvironmentWithNetName</a> and <a href="/previous-versions/windows/desktop/mscs/generic-applications-usenetworkname">UseNetworkName</a>.

## -parameters

### -param lpBuffer [out]

A pointer to a buffer that receives the computer name or the cluster virtual server name. The buffer size should be large enough to contain MAX_COMPUTERNAME_LENGTH + 1 characters.

### -param nSize [in, out]

On input, specifies the size of the buffer, in <b>TCHARs</b>. On output, the number of <b>TCHARs</b> copied to the destination buffer, not including the terminating null character. 




If the buffer is too small, the function fails and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_BUFFER_OVERFLOW. The <i>lpnSize</i> parameter specifies the size of the buffer required, including the terminating null character.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>GetComputerName</b> function retrieves the NetBIOS name established at system startup. Name changes made by the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernamea">SetComputerName</a> or 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa">SetComputerNameEx</a> functions do not take effect until the user restarts the computer.

If the caller is running under a client session, this function returns the server name. To retrieve the client name, use the <a href="/windows/desktop/api/wtsapi32/nf-wtsapi32-wtsquerysessioninformationa">WTSQuerySessionInformation</a> function.


#### Examples

For an example, see 
<a href="/windows/desktop/SysInfo/getting-system-information">Getting System Information</a>.

<div class="code"></div>




> [!NOTE]
> The winbase.h header defines GetComputerName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SysInfo/computer-names">Computer Names</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa">GetComputerNameEx</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernamea">SetComputerName</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa">SetComputerNameEx</a>



<a href="/windows/desktop/SysInfo/system-information-functions">System
    Information Functions</a>
