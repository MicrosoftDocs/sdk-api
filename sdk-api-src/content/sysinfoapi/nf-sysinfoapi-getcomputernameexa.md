---
UID: NF:sysinfoapi.GetComputerNameExA
title: GetComputerNameExA function (sysinfoapi.h)
description: Retrieves a NetBIOS or DNS name associated with the local computer. The names are established at system startup, when the system reads them from the registry. (ANSI)
helpviewer_keywords: ["ComputerNameDnsDomain", "ComputerNameDnsFullyQualified", "ComputerNameDnsHostname", "ComputerNameNetBIOS", "ComputerNamePhysicalDnsDomain", "ComputerNamePhysicalDnsFullyQualified", "ComputerNamePhysicalDnsHostname", "ComputerNamePhysicalNetBIOS", "GetComputerNameExA", "sysinfoapi/GetComputerNameExA"]
old-location: base\getcomputernameex.htm
tech.root: winprog
ms.assetid: eae3f75d-7ec7-42ae-b207-e3ebaa33346e
ms.date: 12/05/2018
ms.keywords: ComputerNameDnsDomain, ComputerNameDnsFullyQualified, ComputerNameDnsHostname, ComputerNameNetBIOS, ComputerNamePhysicalDnsDomain, ComputerNamePhysicalDnsFullyQualified, ComputerNamePhysicalDnsHostname, ComputerNamePhysicalNetBIOS, GetComputerNameEx, GetComputerNameEx function, GetComputerNameExA, GetComputerNameExW, _win32_getcomputernameex, base.getcomputernameex, sysinfoapi/GetComputerNameEx, sysinfoapi/GetComputerNameExA, sysinfoapi/GetComputerNameExW
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetComputerNameExW (Unicode) and GetComputerNameExA (ANSI)
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
 - GetComputerNameExA
 - sysinfoapi/GetComputerNameExA
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
 - GetComputerNameEx
 - GetComputerNameExA
 - GetComputerNameExW
---

## -description

Retrieves a NetBIOS or DNS name associated with the local computer. The names are established at system startup, when the system reads them from the registry.

## -parameters

### -param NameType [in]

The type of name to be retrieved. This parameter is a value from the 
<a href="/windows/desktop/api/sysinfoapi/ne-sysinfoapi-computer_name_format">COMPUTER_NAME_FORMAT</a> enumeration type. The following table provides additional information. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ComputerNameDnsDomain"></a><a id="computernamednsdomain"></a><a id="COMPUTERNAMEDNSDOMAIN"></a><dl>
<dt><b>ComputerNameDnsDomain</b></dt>
</dl>
</td>
<td width="60%">
The name of the DNS domain assigned to the local computer. If the local computer is a node in a cluster, <i>lpBuffer</i> receives the DNS domain name of the cluster virtual server.

</td>
</tr>
<tr>
<td width="40%"><a id="ComputerNameDnsFullyQualified"></a><a id="computernamednsfullyqualified"></a><a id="COMPUTERNAMEDNSFULLYQUALIFIED"></a><dl>
<dt><b>ComputerNameDnsFullyQualified</b></dt>
</dl>
</td>
<td width="60%">
The fully qualified DNS name that uniquely identifies the local computer. This name is a combination of the DNS host name and the DNS domain name, using the form <i>HostName</i>.<i>DomainName</i>. If the local computer is a node in a cluster, <i>lpBuffer</i> receives the fully qualified DNS name of the cluster virtual server.

</td>
</tr>
<tr>
<td width="40%"><a id="ComputerNameDnsHostname"></a><a id="computernamednshostname"></a><a id="COMPUTERNAMEDNSHOSTNAME"></a><dl>
<dt><b>ComputerNameDnsHostname</b></dt>
</dl>
</td>
<td width="60%">
The DNS host name of the local computer. If the local computer is a node in a cluster, <i>lpBuffer</i> receives the DNS host name of the cluster virtual server.

</td>
</tr>
<tr>
<td width="40%"><a id="ComputerNameNetBIOS"></a><a id="computernamenetbios"></a><a id="COMPUTERNAMENETBIOS"></a><dl>
<dt><b>ComputerNameNetBIOS</b></dt>
</dl>
</td>
<td width="60%">
The NetBIOS name of the local computer. If the local computer is a node in a cluster, <i>lpBuffer</i> receives the NetBIOS name of the cluster virtual server.

</td>
</tr>
<tr>
<td width="40%"><a id="ComputerNamePhysicalDnsDomain"></a><a id="computernamephysicaldnsdomain"></a><a id="COMPUTERNAMEPHYSICALDNSDOMAIN"></a><dl>
<dt><b>ComputerNamePhysicalDnsDomain</b></dt>
</dl>
</td>
<td width="60%">
The name of the DNS domain assigned to the local computer. If the local computer is a node in a cluster, <i>lpBuffer</i> receives the DNS domain name of the local computer, not the name of the cluster virtual server.

</td>
</tr>
<tr>
<td width="40%"><a id="ComputerNamePhysicalDnsFullyQualified"></a><a id="computernamephysicaldnsfullyqualified"></a><a id="COMPUTERNAMEPHYSICALDNSFULLYQUALIFIED"></a><dl>
<dt><b>ComputerNamePhysicalDnsFullyQualified</b></dt>
</dl>
</td>
<td width="60%">
The fully qualified DNS name that uniquely identifies the computer. If the local computer is a node in a cluster, <i>lpBuffer</i> receives the fully qualified DNS name of the local computer, not the name of the cluster virtual server. 




The fully qualified DNS name is a combination of the DNS host name and the DNS domain name, using the form <i>HostName</i>.<i>DomainName</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="ComputerNamePhysicalDnsHostname"></a><a id="computernamephysicaldnshostname"></a><a id="COMPUTERNAMEPHYSICALDNSHOSTNAME"></a><dl>
<dt><b>ComputerNamePhysicalDnsHostname</b></dt>
</dl>
</td>
<td width="60%">
The DNS host name of the local computer. If the local computer is a node in a cluster, <i>lpBuffer</i> receives the DNS host name of the local computer, not the name of the cluster virtual server.

</td>
</tr>
<tr>
<td width="40%"><a id="ComputerNamePhysicalNetBIOS"></a><a id="computernamephysicalnetbios"></a><a id="COMPUTERNAMEPHYSICALNETBIOS"></a><dl>
<dt><b>ComputerNamePhysicalNetBIOS</b></dt>
</dl>
</td>
<td width="60%">
The NetBIOS name of the local computer. If the local computer is a node in a cluster, <i>lpBuffer</i> receives the NetBIOS name of the local computer, not the name of the cluster virtual server.

</td>
</tr>
</table>

### -param lpBuffer [out]

A pointer to a buffer that receives the computer name or the cluster virtual server name. 




The length of the name may be greater than MAX_COMPUTERNAME_LENGTH characters because DNS allows longer names. To ensure that this buffer is large enough, set this parameter to <b>NULL</b> and use the required buffer size returned in the <i>lpnSize</i> parameter.

### -param nSize [in, out]

On input, specifies the size of the buffer, in <b>TCHARs</b>. On output, receives the number of <b>TCHARs</b> copied to the destination buffer, not including the terminating <b>null</b> character. 




If the buffer is too small, the function fails and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_MORE_DATA. This parameter receives the size of the buffer required,  including the terminating <b>null</b> character.

If <i>lpBuffer</i> is <b>NULL</b>, this parameter must be zero.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpBuffer</i> buffer is too small. The <i>lpnSize</i> parameter contains the number of bytes required to receive the name.

</td>
</tr>
</table>

## -remarks

If group policy is not set for the local machine, the 
<b>GetComputerNameEx</b> function retrieves the NetBIOS or DNS names established at system startup. If  group policy is set, the function returns the primary domain name set by group policy. Name changes made by the 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernamea">SetComputerName</a> or 
<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa">SetComputerNameEx</a> functions do not take effect until the user restarts the computer.

If the local computer is not configured to use DNS names, <b>GetComputerNameEx</b> will not return DNS information. To configure the computer to do this, follow the steps outlined in the operating system help and change the primary DNS suffix of the computer, then restart the computer. 

The behavior of this function can be affected if the local computer is a node in a cluster. For more information, see <a href="/windows/desktop/api/resapi/nf-resapi-resutilgetenvironmentwithnetname">ResUtilGetEnvironmentWithNetName</a> and <a href="/previous-versions/windows/desktop/mscs/generic-applications-usenetworkname">UseNetworkName</a>.

If you are working with environments that use different DNS layouts, where the computer's FQDN does not match the FQDN of its domain, use <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy">LsaQueryInformationPolicy</a> instead. 

To compile an application that uses this function, define the _WIN32_WINNT macro as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples


```cpp
#define _WIN32_WINNT 0x0500

#include <windows.h>
#include <stdio.h>
#include <tchar.h>

void _tmain(void)
{
    TCHAR buffer[256] = TEXT("");
    TCHAR szDescription[8][32] = {TEXT("NetBIOS"), 
        TEXT("DNS hostname"), 
        TEXT("DNS domain"), 
        TEXT("DNS fully-qualified"), 
        TEXT("Physical NetBIOS"), 
        TEXT("Physical DNS hostname"), 
        TEXT("Physical DNS domain"), 
        TEXT("Physical DNS fully-qualified")};
    int cnf = 0;
    DWORD dwSize = _countof(buffer);
    
    for (cnf = 0; cnf < ComputerNameMax; cnf++)
    {
        if (!GetComputerNameEx((COMPUTER_NAME_FORMAT)cnf, buffer, &dwSize))
        {
            _tprintf(TEXT("GetComputerNameEx failed (%d)\n"), GetLastError());
            return;
        }
        else _tprintf(TEXT("%s: %s\n"), szDescription[cnf], buffer);

        dwSize = _countof(buffer);
        ZeroMemory(buffer, dwSize);
    }
}

```






> [!NOTE]
> The sysinfoapi.h header defines GetComputerNameEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/sysinfoapi/ne-sysinfoapi-computer_name_format">COMPUTER_NAME_FORMAT</a>



<a href="/windows/desktop/SysInfo/computer-names">Computer Names</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getcomputernamea">GetComputerName</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetenvironmentwithnetname">ResUtilGetEnvironmentWithNetName</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetresourceserviceenvironment">ResUtilSetResourceServiceEnvironment</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilsetresourceservicestartparameters">ResUtilSetResourceServiceStartParameters</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernamea">SetComputerName</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa">SetComputerNameEx</a>



<a href="/windows/desktop/SysInfo/system-information-functions">System Information Functions</a>
