---
UID: NF:iphlpapi.CreateIpNetEntry
title: CreateIpNetEntry function (iphlpapi.h)
description: The CreateIpNetEntry function creates an Address Resolution Protocol (ARP) entry in the ARP table on the local computer.
helpviewer_keywords: ["CreateIpNetEntry","CreateIpNetEntry function [IP Helper]","_iphlp_createipnetentry","iphlp.createipnetentry","iphlpapi/CreateIpNetEntry"]
old-location: iphlp\createipnetentry.htm
tech.root: IpHlp
ms.assetid: 607f9aad-2046-4ab2-9a62-4092f87ffa66
ms.date: 12/05/2018
ms.keywords: CreateIpNetEntry, CreateIpNetEntry function [IP Helper], _iphlp_createipnetentry, iphlp.createipnetentry, iphlpapi/CreateIpNetEntry
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - CreateIpNetEntry
 - iphlpapi/CreateIpNetEntry
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
 - CreateIpNetEntry
---

# CreateIpNetEntry function


## -description

The 
<b>CreateIpNetEntry</b> function creates an Address Resolution Protocol (ARP) entry in the ARP table on the local computer.

## -parameters

### -param pArpEntry [in]

A pointer to a 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipnetrow_lh">MIB_IPNETROW</a> structure that specifies information for the new entry. The caller must specify values for all members of this structure.

## -returns

The function returns <b>NO_ERROR</b> (zero) if the function is successful. 

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
Access is denied. This error is returned on Windows Vista and Windows Server 2008 under several conditions that include the following: the  user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (RunAs administrator).  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An input parameter is invalid, no action was taken. This error is returned if the <i>pArpEntry</i> parameter is <b>NULL</b>,  the  <b>dwPhysAddrLen</b> member of 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipnetrow_lh">MIB_IPNETROW</a> is set to zero or a value greater than 8, the <b>&gt;dwAddr</b> member of the <b>MIB_IPNETROW</b> structure is invalid, or one of the other members of the 
<b>MIB_IPNETROW</b> structure is invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The IPv4 transport is not configured on the local computer.

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
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

To modify an existing ARP entry, use the 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipnetentry">SetIpNetEntry</a> function. To retrieve the ARP table, call the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipnettable">GetIpNetTable</a> function. To delete an existing ARP entry, call the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipnetentry">DeleteIpNetEntry</a>.

On Windows Vista and later, the <b>CreateIpNetEntry</b> function can only be called by a user logged on as a member of the Administrators group. If <b>CreateIpNetEntry</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. 

The <b>CreateIpNetEntry</b> function can also fail because of user account control (UAC) on Windows Vista later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.



<div class="alert"><b>Note</b>  On Windows NT 4.0 and Windows 2000 and later, this function executes a privileged operation. For this function to execute successfully, the caller must be logged on as a member of the Administrators group or the NetworkConfigurationOperators group.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createproxyarpentry">CreateProxyArpEntry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipnetentry">DeleteIpNetEntry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteproxyarpentry">DeleteProxyArpEntry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-flushipnettable">FlushIpNetTable</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipnettable">GetIpNetTable</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipnetrow_lh">MIB_IPNETROW</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipnetentry">SetIpNetEntry</a>