---
UID: NF:sysinfoapi.SetComputerNameExW
title: SetComputerNameExW function (sysinfoapi.h)
description: Sets a new NetBIOS or DNS name for the local computer. (Unicode)
helpviewer_keywords: ["ComputerNamePhysicalDnsDomain", "ComputerNamePhysicalDnsHostname", "ComputerNamePhysicalNetBIOS", "SetComputerNameEx", "SetComputerNameEx function", "SetComputerNameExW", "_win32_setcomputernameex", "base.setcomputernameex", "sysinfoapi/SetComputerNameEx", "sysinfoapi/SetComputerNameExW"]
old-location: base\setcomputernameex.htm
tech.root: winprog
ms.assetid: 12163456-770c-4f9e-9261-a6ea5f2cd93a
ms.date: 12/05/2018
ms.keywords: ComputerNamePhysicalDnsDomain, ComputerNamePhysicalDnsHostname, ComputerNamePhysicalNetBIOS, SetComputerNameEx, SetComputerNameEx function, SetComputerNameExA, SetComputerNameExW, _win32_setcomputernameex, base.setcomputernameex, sysinfoapi/SetComputerNameEx, sysinfoapi/SetComputerNameExA, sysinfoapi/SetComputerNameExW
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetComputerNameExW (Unicode) and SetComputerNameExA (ANSI)
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
 - SetComputerNameExW
 - sysinfoapi/SetComputerNameExW
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
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - SetComputerNameEx
 - SetComputerNameExA
 - SetComputerNameExW
---

# SetComputerNameExW function


## -description

Sets a new NetBIOS or DNS name for the local computer. Name changes made by 
<b>SetComputerNameEx</b> do not take effect until the user restarts the computer.

## -parameters

### -param NameType [in]

The type of name to be set. This parameter can be one of the following values from the 
<a href="/windows/desktop/api/sysinfoapi/ne-sysinfoapi-computer_name_format">COMPUTER_NAME_FORMAT</a> enumeration type. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ComputerNamePhysicalDnsDomain"></a><a id="computernamephysicaldnsdomain"></a><a id="COMPUTERNAMEPHYSICALDNSDOMAIN"></a><dl>
<dt><b>ComputerNamePhysicalDnsDomain</b></dt>
</dl>
</td>
<td width="60%">
Sets the primary DNS suffix of the computer.

</td>
</tr>
<tr>
<td width="40%"><a id="ComputerNamePhysicalDnsHostname"></a><a id="computernamephysicaldnshostname"></a><a id="COMPUTERNAMEPHYSICALDNSHOSTNAME"></a><dl>
<dt><b>ComputerNamePhysicalDnsHostname</b></dt>
</dl>
</td>
<td width="60%">
Sets the NetBIOS and the Computer Name (the first label of the full DNS name) to the name specified in <i>lpBuffer</i>. If the name exceeds MAX_COMPUTERNAME_LENGTH characters, the NetBIOS name is truncated to MAX_COMPUTERNAME_LENGTH characters, not including the terminating null character.

</td>
</tr>
<tr>
<td width="40%"><a id="ComputerNamePhysicalNetBIOS"></a><a id="computernamephysicalnetbios"></a><a id="COMPUTERNAMEPHYSICALNETBIOS"></a><dl>
<dt><b>ComputerNamePhysicalNetBIOS</b></dt>
</dl>
</td>
<td width="60%">
Sets the NetBIOS name to the name specified in <i>lpBuffer</i>. The name cannot exceed MAX_COMPUTERNAME_LENGTH characters, not including the terminating null character. 




Warning: Using this option to set the NetBIOS name breaks the convention of interdependent NetBIOS and DNS names. Applications that use the 
<a href="/windows/desktop/api/winbase/nf-winbase-dnshostnametocomputernamea">DnsHostnameToComputerName</a> function to derive the NetBIOS name from the first label of the DNS name will fail if this convention is broken.

</td>
</tr>
</table>

### -param lpBuffer [in]

The new name. The name cannot include control characters, leading or trailing spaces, or any of the following characters: " / \ [ ] : | &lt; &gt; + = ; , ?

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>SetComputerNameEx</b> can set the Computer Name (the first label of the full DNS name) or the primary DNS suffix of the local computer. It cannot set a fully qualified DNS name in one call.

If the local computer is a node in a cluster, 
<b>SetComputerNameEx</b> sets NetBIOS or DNS name of the local computer, not that of the cluster virtual server.

The process that calls the 
<b>SetComputerNameEx</b> function must have administrator privileges on the local computer.

To compile an application that uses this function, define _WIN32_WINNT as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.





> [!NOTE]
> The sysinfoapi.h header defines SetComputerNameEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/sysinfoapi/ne-sysinfoapi-computer_name_format">COMPUTER_NAME_FORMAT</a>



<a href="/windows/desktop/SysInfo/computer-names">Computer Names</a>



<a href="/windows/desktop/api/winbase/nf-winbase-dnshostnametocomputernamea">DnsHostnameToComputerName</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getcomputernamea">GetComputerName</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa">GetComputerNameEx</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernamea">SetComputerName</a>



<a href="/windows/desktop/SysInfo/system-information-functions">System Information Functions</a>
