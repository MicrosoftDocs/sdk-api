---
UID: NF:iphlpapi.GetOwnerModuleFromUdp6Entry
title: GetOwnerModuleFromUdp6Entry function (iphlpapi.h)
description: Retrieves data about the module that issued the context bind for a specific IPv6 UDP endpoint in a MIB table row.
helpviewer_keywords: ["GetOwnerModuleFromUdp6Entry","GetOwnerModuleFromUdp6Entry function [IP Helper]","iphlp.getownermodulefromudp6entry","iphlpapi/GetOwnerModuleFromUdp6Entry"]
old-location: iphlp\getownermodulefromudp6entry.htm
tech.root: IpHlp
ms.assetid: 01ed27b6-3ca6-4c9c-8910-a71a073c2ca2
ms.date: 12/05/2018
ms.keywords: GetOwnerModuleFromUdp6Entry, GetOwnerModuleFromUdp6Entry function [IP Helper], iphlp.getownermodulefromudp6entry, iphlpapi/GetOwnerModuleFromUdp6Entry
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetOwnerModuleFromUdp6Entry
 - iphlpapi/GetOwnerModuleFromUdp6Entry
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetOwnerModuleFromUdp6Entry
---

# GetOwnerModuleFromUdp6Entry function


## -description

The <b>GetOwnerModuleFromUdp6Entry</b> function retrieves data about the module that issued the context bind for a specific IPv6 UDP endpoint in a MIB table row.

## -parameters

### -param pUdpEntry [in]

A pointer to a <a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6row_owner_module">MIB_UDP6ROW_OWNER_MODULE</a> structure that contains the IPv6 UDP endpoint entry used to obtain the owner module.

### -param Class [in]

<a href="/windows/desktop/api/iprtrmib/ne-iprtrmib-tcpip_owner_module_info_class">TCPIP_OWNER_MODULE_INFO_CLASS</a> enumeration value that indicates the type of data to obtain regarding the owner module.

### -param pBuffer [out]

The buffer that contains a <a href="/windows/desktop/api/iprtrmib/ns-iprtrmib-tcpip_owner_module_basic_info">TCPIP_OWNER_MODULE_BASIC_INFO</a> structure with the owner module data. The type of data returned in this buffer is indicated by the value of the <i>Class</i> parameter.

The following structures are used for the data in <i>Buffer</i> when  <i>Class</i> is set to the corresponding value.

<table>
<tr>
<th><i>Class</i> enumeration value</th>
<th><i>Buffer</i> data format</th>
</tr>
<tr>
<td>TCPIP_OWNER_MODULE_BASIC_INFO</td>
<td>
<a href="/windows/desktop/api/iprtrmib/ns-iprtrmib-tcpip_owner_module_basic_info">TCPIP_OWNER_MODULE_BASIC_INFO</a>
</td>
</tr>
</table>

### -param pdwSize [in, out]

The estimated size, in bytes, of the structure returned in <i>Buffer</i>. If this value is set too small, <b>ERROR_INSUFFICIENT_BUFFER</b> is returned by this function, and this field will contain the correct size of the structure.

## -returns

If the call is successful, the value <b>NO_ERROR</b> is returned. Otherwise, the following error is returned.

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
An insufficient amount of space was allocated for the table. The size of the table is returned in the <i>pdwSize</i> parameter, and must be used in a subsequent call to this function in order to successfully retrieve the table.

</td>
</tr>
</table>

## -remarks

The <i>Buffer</i> parameter contains not only a structure with pointers to specific data, for example, pointers to the zero-terminated strings that contain the name and path of the owner module, but the actual data itself; that is the name and path strings. Therefore, when calculating the buffer size, ensure that you have enough space for both the structure as well as the data the members of the structure point to.

The resolution of UDP table entries to owner modules is a best practice. In a few cases, the owner module name returned in the <a href="/windows/desktop/api/iprtrmib/ns-iprtrmib-tcpip_owner_module_basic_info">TCPIP_OWNER_MODULE_BASIC_INFO</a> structure can be a process name, such as "svchost.exe", a service name, such as "RPC", or a component name, such as "timer.dll".

For computers running on Windows Vista or later, accessing the <b>pModuleName</b> and <b>pModulePath</b> members of the <a href="/windows/desktop/api/iprtrmib/ns-iprtrmib-tcpip_owner_module_basic_info">TCPIP_OWNER_MODULE_BASIC_INFO</a> structure is limited  by user account control (UAC). If an application that calls this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will succeed but access to these members returns an empty string unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application on Windows Vista or later lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for access to the protected <b>pModuleName</b> and <b>pModulePath</b> members to be allowed.