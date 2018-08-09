---
UID: NF:iphlpapi.SetIpStatisticsEx
title: SetIpStatisticsEx function
author: windows-sdk-content
description: Toggles IP forwarding on or off and sets the default time-to-live (TTL) value for the local computer.
old-location: iphlp\setipstatisticsex.htm
old-project: iphlp
ms.assetid: 13b52016-5bdb-4546-af53-d3ae2708653b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: AF_INET, AF_INET6, SetIpStatisticsEx, SetIpStatisticsEx function [IP Helper], iphlp.setipstatisticsex, iphlpapi/SetIpStatisticsEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NET_ADDRESS_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - SetIpStatisticsEx
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# SetIpStatisticsEx function


## -description


The 
<b>SetIpStatisticsEx</b> function toggles IP forwarding on or off and sets the default time-to-live (TTL) value for the local computer.


## -parameters




### -param Statistics [in]

A pointer to a 
<a href="https://msdn.microsoft.com/920e71b6-247c-4442-9f66-704a6c878feb">MIB_IPSTATS</a> structure. The caller should set the <b>dwForwarding</b> and <b>dwDefaultTTL</b> members of this structure to the new values. To keep one of the members at its current value, use MIB_USE_CURRENT_TTL or MIB_USE_CURRENT_FORWARDING.


### -param Family

The address family for which forwarding and TTL is to be set. 

Possible values for the address family are listed in the <i>Winsock2.h</i> header file. Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_INET</b> and <b>PF_INET</b>), so either constant can be used.

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and possible values for this member are defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

The values currently supported are <b>AF_INET</b>, and <b>AF_INET6</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 4 (IPv4) address family. When this parameter is specified,  this function  sets forwarding and TTL options for IPv4 entries. 

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 6 (IPv6) address family. When this parameter is specified,  this function  sets forwarding and TTL options for IPv6 entries. 

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
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>pIpStats</i> parameter or the <i>Family</i> parameter was not set to <b>AF_INET</b>, and <b>AF_INET6</b>. This error is also returned if the <b>dwForwarding</b> member in the <a href="https://msdn.microsoft.com/920e71b6-247c-4442-9f66-704a6c878feb">MIB_IPSTATS</a> structure pointed to by the <i>pIpStats</i> parameter contains a value other than <b>MIB_IP_NOT_FORWARDING</b>, <b>MIB_IP_FORWARDING</b>, or <b>MIB_USE_CURRENT_FORWARDING</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer and AF_INET was specified in the <i>Family</i> parameter or no IPv6 stack is on the local computer and AF_INET6 was specified in the <i>Family</i> member.

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



To set only the default TTL, the caller can also use the 
<a href="https://msdn.microsoft.com/dfde8712-f68f-4fa4-b939-ea36e23b5b1e">SetIpTTL</a> function.

The <b>SetIpStatisticsEx</b> function can only be called by a user logged on as a member of the Administrators group. If <b>SetIpStatisticsEx</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. 

The <b>SetIpStatisticsEx</b> function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application on lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.






## -see-also




<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/920e71b6-247c-4442-9f66-704a6c878feb">MIB_IPSTATS</a>



<a href="https://msdn.microsoft.com/d857ee04-38b8-4d98-a3e7-6ca8657ac9ed">SetIpStatistics</a>



<a href="https://msdn.microsoft.com/dfde8712-f68f-4fa4-b939-ea36e23b5b1e">SetIpTTL</a>
 

 

