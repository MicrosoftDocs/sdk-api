---
UID: NF:netioapi.FlushIpPathTable
title: FlushIpPathTable function
author: windows-sdk-content
description: The FlushIpPathTable function flushes the IP path table on the local computer.
old-location: iphlp\flushippathtable.htm
tech.root: IpHlp
ms.assetid: 3b28e0cd-9cab-41ca-b58c-7632768318c2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AF_INET, AF_INET6, AF_UNSPEC, FlushIpPathTable, FlushIpPathTable function [IP Helper], iphlp.flushippathtable, netioapi/FlushIpPathTable
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - FlushIpPathTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- FlushIpPathTable
: 
---

# FlushIpPathTable function


## -description


The 
<b>FlushIpPathTable</b> function flushes the IP path table on the local computer.


## -parameters




### -param Family [in]

The address family to flush. 

Possible values for the address family are listed in the <i>Winsock2.h</i> header file. Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_INET</b> and <b>PF_INET</b>), so either constant can be used.

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and possible values for this member are defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

The values currently supported are <b>AF_INET</b>, <b>AF_INET6</b>, and <b>AF_UNSPEC</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_UNSPEC"></a><a id="af_unspec"></a><dl>
<dt><b>AF_UNSPEC</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The address family is unspecified. When this parameter is specified,  this function  flushes the IP path table containing both IPv4 and IPv6 entries. 

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 4 (IPv4) address family. When this parameter is specified,  this function  flushes the IP path table containing only  IPv4 entries. 

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 6 (IPv6) address family. When this parameter is specified,  this function  flushes the IP path table containing only IPv6 entries. 

</td>
</tr>
</table>
 


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. This error is returned under several conditions that include the following: the  user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (RunAs administrator).  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if the <i>Family</i> parameter was not specified as <b>AF_INET</b>, <b>AF_INET6</b>, or <b>AF_UNSPEC</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer and <b>AF_INET</b> was specified in the <b>Family</b> parameter. This error is also returned if no IPv6 stack is on the local computer and <b>AF_INET6</b> was specified in the <b>Family</b> parameter. This error is also returned on versions of Windows where this function is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>FlushIpPathTable</b> function is defined on Windows Vista and later. 

The  
<b>FlushIpPathTable</b> function flushes or deletes the IP path entries on a local system.  The <i>Family</i> parameter can be used to limit the IP path entries to delete to a particular IP address family. If IP path entries for both IPv4 and IPv6 should be deleted, set the  <i>Family</i> parameter to <b>AF_UNSPEC</b>. 

The <i>Family</i> parameter must be initialized to either <b>AF_INET</b>,  <b>AF_INET6</b>, or <b>AF_UNSPEC</b>. 

The <b>FlushIpPathTable</b> function can only be called by a user logged on as a member of the Administrators group. If <b>FlushIpPathTable</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.






## -see-also




<a href="https://msdn.microsoft.com/8ad43a1d-428a-41cc-bba8-5eec7f87c11f">GetIpPathEntry</a>



<a href="https://msdn.microsoft.com/e03816a4-0b86-4e0b-a45e-8148c8ba5472">GetIpPathTable</a>



<a href="https://msdn.microsoft.com/0cfef3cb-bb96-4250-864b-2468a46ba277">MIB_IPPATH_ROW</a>



<a href="https://msdn.microsoft.com/f18aff3c-a7b5-40fa-9308-5bd8821c77e2">MIB_IPPATH_TABLE</a>
 

 

