---
UID: NF:winbase.DnsHostnameToComputerNameA
title: DnsHostnameToComputerNameA function
author: windows-sdk-content
description: Converts a DNS-style host name to a NetBIOS-style computer name.
old-location: base\dnshostnametocomputername.htm
tech.root: sysinfo
ms.assetid: d5646fe6-9112-42cd-ace9-00dd1b590ecb
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DnsHostnameToComputerName, DnsHostnameToComputerName function, DnsHostnameToComputerNameA, DnsHostnameToComputerNameW, _win32_dnshostnametocomputername, base.dnshostnametocomputername, winbase/DnsHostnameToComputerName, winbase/DnsHostnameToComputerNameA, winbase/DnsHostnameToComputerNameW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DnsHostnameToComputerNameA function


## -description


Converts a DNS-style host name to a NetBIOS-style computer name.


## -parameters




### -param Hostname [in]

The DNS name. If the DNS name is not a valid, translatable name, the function fails. For more information, see <a href="https://msdn.microsoft.com/7e083cb5-cf0a-4284-8b54-dac856910c44">Computer Names</a>.


### -param ComputerName [out]

A pointer to a buffer that receives the computer name. The buffer size should be large enough to contain MAX_COMPUTERNAME_LENGTH + 1 characters.


### -param nSize [in, out]

On input, specifies the size of the buffer, in <b>TCHARs</b>. On output, receives the number of <b>TCHARs</b> copied to the destination buffer, not including the terminating null character. 




If the buffer is too small, the function fails, <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns ERROR_MORE_DATA, and <i>nSize</i> receives the required buffer size, not including the terminating null character.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. Possible values include the following.

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
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/eae3f75d-7ec7-42ae-b207-e3ebaa33346e">GetComputerNameEx</a>



<a href="https://msdn.microsoft.com/12163456-770c-4f9e-9261-a6ea5f2cd93a">SetComputerNameEx</a>



<a href="https://msdn.microsoft.com/aa7deebf-7dce-4147-8a15-1d7411aea0fa">System
    Information Functions</a>
 

 

