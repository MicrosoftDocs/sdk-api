---
UID: NF:iphlpapi.CreateProxyArpEntry
title: CreateProxyArpEntry function (iphlpapi.h)
description: The CreateProxyArpEnry function creates a Proxy Address Resolution Protocol (PARP) entry on the local computer for the specified IPv4 address.
helpviewer_keywords: ["CreateProxyArpEntry","CreateProxyArpEntry function [IP Helper]","_iphlp_createproxyarpentry","iphlp.createproxyarpentry","iphlpapi/CreateProxyArpEntry"]
old-location: iphlp\createproxyarpentry.htm
tech.root: IpHlp
ms.assetid: a0e90c0a-9403-40cb-906e-6e1e2f8e73c4
ms.date: 12/05/2018
ms.keywords: CreateProxyArpEntry, CreateProxyArpEntry function [IP Helper], _iphlp_createproxyarpentry, iphlp.createproxyarpentry, iphlpapi/CreateProxyArpEntry
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
 - CreateProxyArpEntry
 - iphlpapi/CreateProxyArpEntry
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
 - CreateProxyArpEntry
---

# CreateProxyArpEntry function


## -description

The <b>CreateProxyArpEnry</b> function creates a Proxy Address Resolution Protocol (PARP) entry on the local computer for the specified IPv4 address.

## -parameters

### -param dwAddress [in]

The IPv4 address for which this computer acts as a proxy.

### -param dwMask [in]

The subnet mask for the IPv4 address specified in <i>dwAddress</i>.

### -param dwIfIndex [in]

The index of the interface on which to proxy ARP for the IPv4 address identified by <i>dwAddress</i>. In other words, when an ARP request for <i>dwAddress</i> is received on this interface, the local computer responds with the physical address of this interface. If this interface is of a type that does not support ARP, such as PPP, then the call fails.

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
An input parameter is invalid, no action was taken. This error is returned if the <i>dwAddress</i> parameter is <b>zero</b> or an invalid value,  one of the other parameters is invalid. 

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

To retrieve the ARP table, call the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipnettable">GetIpNetTable</a> function. To delete an existing PARP entry, call the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteproxyarpentry">DeleteProxyArpEntry</a>.

On Windows Vista and later, the <b>CreateProxyArpEnry</b> function can only be called by a user logged on as a member of the Administrators group. If <b>CreateProxyArpEnry</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application on Windows Vista and later lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.



<div class="alert"><b>Note</b>  This function executes a privileged operation. For this function to execute successfully, the caller must be logged on as a member of the Administrators group or the NetworkConfigurationOperators group.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteproxyarpentry">DeleteProxyArpEntry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipnettable">GetIpNetTable</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_proxyarp">MIB_PROXYARP</a>