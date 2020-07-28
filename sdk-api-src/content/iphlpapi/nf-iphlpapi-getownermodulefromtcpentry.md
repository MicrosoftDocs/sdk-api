---
UID: NF:iphlpapi.GetOwnerModuleFromTcpEntry
title: GetOwnerModuleFromTcpEntry function (iphlpapi.h)
description: Retrieves data about the module that issued the context bind for a specific IPv4 TCP endpoint in a MIB table row.
helpviewer_keywords: ["GetOwnerModuleFromTcpEntry","GetOwnerModuleFromTcpEntry function [IP Helper]","iphlp.getownermodulefromtcpentry","iphlpapi/GetOwnerModuleFromTcpEntry"]
old-location: iphlp\getownermodulefromtcpentry.htm
tech.root: IpHlp
ms.assetid: 12162f0a-56c1-4f81-a1f5-3cd5ad975d0d
ms.date: 12/05/2018
ms.keywords: GetOwnerModuleFromTcpEntry, GetOwnerModuleFromTcpEntry function [IP Helper], iphlp.getownermodulefromtcpentry, iphlpapi/GetOwnerModuleFromTcpEntry
f1_keywords:
- iphlpapi/GetOwnerModuleFromTcpEntry
dev_langs:
- c++
req.header: iphlpapi.h
req.include-header: 
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Iphlpapi.dll
api_name:
- GetOwnerModuleFromTcpEntry
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetOwnerModuleFromTcpEntry function


## -description


The <b>GetOwnerModuleFromTcpEntry</b> function retrieves data about the module that issued the context bind for a specific IPv4 TCP endpoint in a MIB table row.


## -parameters




### -param pTcpEntry [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow_owner_module">MIB_TCPROW_OWNER_MODULE</a> structure that contains the IPv4 TCP endpoint entry used to obtain the owner module.


### -param Class [in]

 A <a href="https://docs.microsoft.com/windows/desktop/api/iprtrmib/ne-iprtrmib-tcpip_owner_module_info_class">TCPIP_OWNER_MODULE_INFO_CLASS</a> enumeration value that indicates the type of data to obtain regarding the owner module. The <b>TCPIP_OWNER_MODULE_INFO_CLASS</b> enumeration is defined in the <i>Iprtrmib.h</i> header file.

 This parameter must be set to <b>TCPIP_OWNER_MODULE_INFO_BASIC</b>.


### -param pBuffer [out]

A pointer a buffer that contains a <a href="https://docs.microsoft.com/windows/desktop/api/iprtrmib/ns-iprtrmib-tcpip_owner_module_basic_info">TCPIP_OWNER_MODULE_BASIC_INFO</a> structure with the owner module data. The type of data returned in this buffer is indicated by the value of the <i>Class</i> parameter. 

The following structures are used for the data in <i>Buffer</i> when  <i>Class</i> is set to the corresponding value.

<table>
<tr>
<th><i>Class</i> enumeration value</th>
<th><i>Buffer</i> data format</th>
</tr>
<tr>
<td>TCPIP_OWNER_MODULE_BASIC_INFO</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/iprtrmib/ns-iprtrmib-tcpip_owner_module_basic_info">TCPIP_OWNER_MODULE_BASIC_INFO</a>
</td>
</tr>
</table>
 


### -param pdwSize [in, out]

The estimated size, in  bytes, of the structure returned in <i>Buffer</i>. If this value is set too small, <b>ERROR_INSUFFICIENT_BUFFER</b> is returned by this function, and this field will contain the correct size of the buffer. The size required is the size of the corresponding structure plus an additional number of bytes equal to the length of data pointed to in the structure (for example, the name and path strings).


## -returns



If the function call is successful, the value <b>NO_ERROR</b> is returned. 

If the function fails, the return value is one of the following error codes.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
Insufficient space was allocated for the table. The size of the table is returned in the <i>pdwSize</i> parameter, and must be used in a subsequent call to this function in order to successfully retrieve the table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This value is returned if either of the <i>pTcpEntry</i> or <i>pdwSize</i> parameters are <b>NULL</b>. This value is also returned if the <i>Class</i> parameter is not equal to <b>TCPIP_OWNER_MODULE_INFO_BASIC</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
A element was no found. This value is returned if the <b>dwOwningPid</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow_owner_module">MIB_TCPROW_OWNER_MODULE</a> structure pointed to by the <i>pTcpEntry</i> parameter was zero or could not be found. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PARTIAL_COPY</b></dt>
</dl>
</td>
<td width="60%">
Only part of a request was completed.

</td>
</tr>
</table>
 




## -remarks



The <i>Buffer</i> parameter contains not only a structure with pointers to specific data,  for example, pointers to the zero-terminated strings that contain the name and path of the owner module, but the actual data itself; that is the name and path strings. Therefore, when calculating the buffer size, ensure that you have enough space for both the structure as well as the data the members of the structure point to.

The resolution of TCP table entries to owner modules is a best practice. In a few cases, the owner module name returned in the <a href="https://docs.microsoft.com/windows/desktop/api/iprtrmib/ns-iprtrmib-tcpip_owner_module_basic_info">TCPIP_OWNER_MODULE_BASIC_INFO</a> structure can be a process name, such as "svchost.exe", a service name (such as "RPC"), or a component name, such as "timer.dll".

For computers running on Windows Vista or later, the <b>pModuleName</b> and <b>pModulePath</b> members of the <a href="https://docs.microsoft.com/windows/desktop/api/iprtrmib/ns-iprtrmib-tcpip_owner_module_basic_info">TCPIP_OWNER_MODULE_BASIC_INFO</a> retrieved by  <b>GetOwnerModuleFromTcpEntry</b> function may point to an empty string for some TCP connections. Applications that start TCP connections located in the Windows system folder (C:\Windows\System32, by default) are considered protected. If the <b>GetOwnerModuleFromTcpEntry</b> function is called by a user that is not a member of the Administrators group, the function call will succeed but the <b>pModuleName</b> and <b>pModulePath</b> members will point to memory that contains an empty string for the TCP connections started by protected applications. 

For computers running on Windows Vista or later, accessing the <b>pModuleName</b> and <b>pModulePath</b> members of the <a href="https://docs.microsoft.com/windows/desktop/api/iprtrmib/ns-iprtrmib-tcpip_owner_module_basic_info">TCPIP_OWNER_MODULE_BASIC_INFO</a> structure is limited  by user account control (UAC). If an application that calls this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will succeed but access to these members returns an empty string unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application on Windows Vista or later lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for access to the protected <b>pModuleName</b> and <b>pModulePath</b> members to be allowed. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcprow_owner_module">MIB_TCPROW_OWNER_MODULE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iprtrmib/ns-iprtrmib-tcpip_owner_module_basic_info">TCPIP_OWNER_MODULE_BASIC_INFO</a>
 

 

