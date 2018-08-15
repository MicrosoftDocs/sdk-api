---
UID: NF:netioapi.GetIpPathEntry
title: GetIpPathEntry function
author: windows-sdk-content
description: Retrieves information for a IP path entry on the local computer.
old-location: iphlp\getippathentry.htm
old-project: iphlp
ms.assetid: 8ad43a1d-428a-41cc-bba8-5eec7f87c11f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetIpPathEntry, GetIpPathEntry function [IP Helper], iphlp.getippathentry, netioapi/GetIpPathEntry
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.redist: 
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
tech.root: 
req.typenames: MIB_NOTIFICATION_TYPE, *PMIB_NOTIFICATION_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetIpPathEntry
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# GetIpPathEntry function


## -description


The 
<b>GetIpPathEntry</b> function  retrieves information for a IP path entry on the local computer. 


## -parameters




### -param Row [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/0cfef3cb-bb96-4250-864b-2468a46ba277">MIB_IPPATH_ROW</a> structure entry for a IP path entry. On successful return, this structure will be updated with the properties for IP path entry.


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
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The system cannot find the file specified. This error is returned if the  network interface LUID or interface index specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="https://msdn.microsoft.com/0cfef3cb-bb96-4250-864b-2468a46ba277">MIB_IPPATH_ROW</a> pointed to by the <i>Row</i> parameter is not a value on the local machine.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if a <b>NULL</b> pointer is passed in the <i>Row</i> parameter, the <b>si_family</b> member in the <b>Destination</b> member of the <a href="https://msdn.microsoft.com/0cfef3cb-bb96-4250-864b-2468a46ba277">MIB_IPPATH_ROW</a> pointed to by the <i>Row</i> parameter is not set to <b>AF_INET</b> or <b>AF_INET6</b>, or both the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> members of the <b>MIB_IPPATH_ROW</b> pointed to by the <i>Row</i> parameter are unspecified. This error is also returned if the <b>si_family</b> member in the <b>Source</b> member of the <b>MIB_IPPATH_ROW</b> pointed to by the <i>Row</i> parameter did not match the destination IP address family and the <b>si_family</b> for the source IP address is not specified as <b>AF_UNSPEC</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Element not found. This error is returned if the  network interface specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="https://msdn.microsoft.com/0cfef3cb-bb96-4250-864b-2468a46ba277">MIB_IPPATH_ROW</a> structure pointed to by the <i>Row</i> parameter does not match the IP address and address family specified in the <b>Destination</b> member in the <b>MIB_IPPATH_ROW</b> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer and an IPv4 address is specified in the <b>Source</b> and <b>Destination</b> members of the <a href="https://msdn.microsoft.com/0cfef3cb-bb96-4250-864b-2468a46ba277">MIB_IPPATH_ROW</a> pointed to by the <i>Row</i> parameter. This error is also returned if no IPv6 stack is on the local computer and an IPv6 address is specified in the <b>Source</b> and <b>Destination</b> members. 

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



The <b>GetIpPathEntry</b> function is defined on Windows Vista and later. 

The <b>GetIpPathEntry</b> function is used to retrieve a <a href="https://msdn.microsoft.com/0cfef3cb-bb96-4250-864b-2468a46ba277">MIB_IPPATH_ROW</a> structure entry.  

On input, the <b>Destination</b> member in the <a href="https://msdn.microsoft.com/0cfef3cb-bb96-4250-864b-2468a46ba277">MIB_IPPATH_ROW</a> structure pointed to by the <i>Row</i> parameter must be initialized to a valid IPv4 or IPv6 address and family. The address family specified in <b>Source</b> member in the <b>MIB_IPPATH_ROW</b> structure must also either match the destination IP address family specified in the <b>Destination</b> member or the address family in the <b>Source</b> member must be specified as <b>AF_UNSPEC</b>. In addition , at least one of the following members in the <b>MIB_IPPATH_ROW</b> structure pointed to the <i>Row</i> parameter must be initialized:
    the <b>InterfaceLuid</b> or <b>InterfaceIndex</b>.

    The fields are used in the order listed above. So if the <b>InterfaceLuid</b> is specified, then this member is used to determine the interface. If no value is set for the  <b>InterfaceLuid</b> member (the values of this member is set to zero), then the <b>InterfaceIndex</b> member is next used to determine the interface. 

On output when the call is successful, <b>GetIpPathEntry</b> retrieves the other properties for the IP path entry and fills out the <a href="https://msdn.microsoft.com/0cfef3cb-bb96-4250-864b-2468a46ba277">MIB_IPPATH_ROW</a> structure pointed to by the <i>Row</i> parameter. 

The <a href="https://msdn.microsoft.com/e03816a4-0b86-4e0b-a45e-8148c8ba5472">GetIpPathTable</a> function can be called to enumerate the IP path entries on a local computer.




## -see-also




<a href="https://msdn.microsoft.com/3b28e0cd-9cab-41ca-b58c-7632768318c2">FlushIpPathTable</a>



<a href="https://msdn.microsoft.com/e03816a4-0b86-4e0b-a45e-8148c8ba5472">GetIpPathTable</a>



<a href="https://msdn.microsoft.com/0cfef3cb-bb96-4250-864b-2468a46ba277">MIB_IPPATH_ROW</a>



<a href="https://msdn.microsoft.com/f18aff3c-a7b5-40fa-9308-5bd8821c77e2">MIB_IPPATH_TABLE</a>
 

 

