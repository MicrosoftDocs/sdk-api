---
UID: NF:winbase.DnsHostnameToComputerNameW
title: DnsHostnameToComputerNameW function (winbase.h)
description: Converts a DNS-style host name to a NetBIOS-style computer name. (Unicode)
helpviewer_keywords: ["DnsHostnameToComputerName", "DnsHostnameToComputerName function", "DnsHostnameToComputerNameW", "_win32_dnshostnametocomputername", "base.dnshostnametocomputername", "winbase/DnsHostnameToComputerName", "winbase/DnsHostnameToComputerNameW"]
old-location: base\dnshostnametocomputername.htm
tech.root: winprog
ms.assetid: d5646fe6-9112-42cd-ace9-00dd1b590ecb
ms.date: 12/05/2018
ms.keywords: DnsHostnameToComputerName, DnsHostnameToComputerName function, DnsHostnameToComputerNameA, DnsHostnameToComputerNameW, _win32_dnshostnametocomputername, base.dnshostnametocomputername, winbase/DnsHostnameToComputerName, winbase/DnsHostnameToComputerNameA, winbase/DnsHostnameToComputerNameW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DnsHostnameToComputerNameW (Unicode) and DnsHostnameToComputerNameA (ANSI)
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
 - DnsHostnameToComputerNameW
 - winbase/DnsHostnameToComputerNameW
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
 - DnsHostnameToComputerName
 - DnsHostnameToComputerNameA
 - DnsHostnameToComputerNameW
---

# DnsHostnameToComputerNameW function


## -description

Converts a DNS-style host name to a NetBIOS-style computer name.

## -parameters

### -param Hostname [in]

The DNS name. If the DNS name is not a valid, translatable name, the function fails. For more information, see <a href="/windows/desktop/SysInfo/computer-names">Computer Names</a>.

### -param ComputerName [out]

A pointer to a buffer that receives the computer name. The buffer size should be large enough to contain MAX_COMPUTERNAME_LENGTH + 1 characters.

### -param nSize [in, out]

On input, specifies the size of the buffer, in <b>TCHARs</b>. On output, receives the number of <b>TCHARs</b> copied to the destination buffer, not including the terminating null character. 




If the buffer is too small, the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns ERROR_MORE_DATA, and <i>nSize</i> receives the required buffer size, not including the terminating null character.

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
The <i>ComputerName</i> buffer is too small. The <i>nSize</i> parameter contains the number of bytes required to receive the name.

</td>
</tr>
</table>

## -remarks

This function performs a textual mapping of the name. This convention limits the names of computers to be the common subset of the names. (Specifically, the leftmost label of the DNS name is truncated to 15-bytes of OEM characters.) Therefore, do not use this function to convert a DNS domain name to a NetBIOS domain name. There is no textual mapping for domain names.

To compile an application that uses this function, define _WIN32_WINNT as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.





> [!NOTE]
> The winbase.h header defines DnsHostnameToComputerName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa">GetComputerNameEx</a>



<a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-setcomputernameexa">SetComputerNameEx</a>



<a href="/windows/desktop/SysInfo/system-information-functions">System
    Information Functions</a>
