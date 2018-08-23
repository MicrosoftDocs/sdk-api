---
UID: NF:sysinfoapi.SetComputerNameExA
title: SetComputerNameExA function
author: windows-sdk-content
description: Sets a new NetBIOS or DNS name for the local computer.
old-location: base\setcomputernameex.htm
old-project: sysinfo
ms.assetid: 12163456-770c-4f9e-9261-a6ea5f2cd93a
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: ComputerNamePhysicalDnsDomain, ComputerNamePhysicalDnsHostname, ComputerNamePhysicalNetBIOS, SetComputerNameEx, SetComputerNameEx function, SetComputerNameExA, SetComputerNameExW, _win32_setcomputernameex, base.setcomputernameex, sysinfoapi/SetComputerNameEx, sysinfoapi/SetComputerNameExA, sysinfoapi/SetComputerNameExW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: sysinfoapi.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: COMPUTER_NAME_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# SetComputerNameExA function


## -description


Sets a new NetBIOS or DNS name for the local computer. Name changes made by 
<b>SetComputerNameEx</b> do not take effect until the user restarts the computer.


## -parameters




### -param NameType [in]

The type of name to be set. This parameter can be one of the following values from the 
<a href="https://msdn.microsoft.com/249830be-acd7-4417-ac33-c0fb2d87c4af">COMPUTER_NAME_FORMAT</a> enumeration type. 



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
<a href="https://msdn.microsoft.com/d5646fe6-9112-42cd-ace9-00dd1b590ecb">DnsHostnameToComputerName</a> function to derive the NetBIOS name from the first label of the DNS name will fail if this convention is broken.

</td>
</tr>
</table>
 


### -param lpBuffer [in]

The new name. The name cannot include control characters, leading or trailing spaces, or any of the following characters: " / \ [ ] : | &lt; &gt; + = ; , ?


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>SetComputerNameEx</b> can set the Computer Name (the first label of the full DNS name) or the primary DNS suffix of the local computer. It cannot set a fully qualified DNS name in one call.

If the local computer is a node in a cluster, 
<b>SetComputerNameEx</b> sets NetBIOS or DNS name of the local computer, not that of the cluster virtual server.

The process that calls the 
<b>SetComputerNameEx</b> function must have administrator privileges on the local computer.

To compile an application that uses this function, define _WIN32_WINNT as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/249830be-acd7-4417-ac33-c0fb2d87c4af">COMPUTER_NAME_FORMAT</a>



<a href="https://msdn.microsoft.com/7e083cb5-cf0a-4284-8b54-dac856910c44">Computer Names</a>



<a href="https://msdn.microsoft.com/d5646fe6-9112-42cd-ace9-00dd1b590ecb">DnsHostnameToComputerName</a>



<a href="https://msdn.microsoft.com/8ca3e611-e5fb-4909-adf6-98eb8552c9e1">GetComputerName</a>



<a href="https://msdn.microsoft.com/eae3f75d-7ec7-42ae-b207-e3ebaa33346e">GetComputerNameEx</a>



<a href="https://msdn.microsoft.com/ff64fde2-d1b5-4211-b8c4-4823a5469e04">SetComputerName</a>



<a href="https://msdn.microsoft.com/aa7deebf-7dce-4147-8a15-1d7411aea0fa">System Information Functions</a>
 

 

