---
UID: NF:iphlpapi.GetBestInterfaceEx
title: GetBestInterfaceEx function (iphlpapi.h)
description: The GetBestInterfaceEx function retrieves the index of the interface that has the best route to the specified IPv4 or IPv6 address.
helpviewer_keywords: ["GetBestInterfaceEx","GetBestInterfaceEx function [IP Helper]","iphlp.getbestinterfaceex","iphlpapi/GetBestInterfaceEx"]
old-location: iphlp\getbestinterfaceex.htm
tech.root: IpHlp
ms.assetid: cfd1108e-d7a0-4fe5-be3f-299189089d37
ms.date: 12/05/2018
ms.keywords: GetBestInterfaceEx, GetBestInterfaceEx function [IP Helper], iphlp.getbestinterfaceex, iphlpapi/GetBestInterfaceEx
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - GetBestInterfaceEx
 - iphlpapi/GetBestInterfaceEx
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
 - GetBestInterfaceEx
---

# GetBestInterfaceEx function


## -description

The 
<b>GetBestInterfaceEx</b> function retrieves the index of the interface that has the best route to the specified IPv4 or IPv6 address.

## -parameters

### -param pDestAddr [in]

The destination IPv6 or IPv4 address for which to retrieve the interface with the best route, in the form of a <a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a> structure.

### -param pdwBestIfIndex [out]

A pointer to the index of the interface with the best route to the IPv6 or IPv4 address specified by <i>pDestAddr</i>.

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
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The operation could not be completed. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>pdwBestIfIndex</i> parameter or if the <i>pDestAddr </i> or <i>pdwBestIfIndex</i> parameters point to memory that cannot be accessed. This error can also be returned if the <i>pdwBestIfIndex</i> parameter points to memory that can't be written to.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer and an IPv4 address was specified in the <i>pDestAddr</i> parameter or no IPv6 stack is on the local computer and an IPv6 address was specified in the <i>pDestAddr</i> parameter.

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
the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>GetBestInterfaceEx</b> function differs from the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestinterface">GetBestInterface</a> function in that it can be used with either IPv4 or IPv6 addresses.

The <b>Family</b> member of the sockaddr structure pointed to by the <i>pDestAddr</i> parameter must be set to one of the following values: <b>AF_INET</b> or <b>AF_INET6</b>. 

On Windows Vista and later, the <i>pdwBestIfIndex</i> parameter is treated internally by IP Helper as a pointer to a <b>NET_IFINDEX</b> datatype.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestinterface">GetBestInterface</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_best_if">MIB_BEST_IF</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>