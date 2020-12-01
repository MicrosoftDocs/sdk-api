---
UID: NF:iphlpapi.GetBestInterface
title: GetBestInterface function (iphlpapi.h)
description: The GetBestInterface function retrieves the index of the interface that has the best route to the specified IPv4 address.
helpviewer_keywords: ["GetBestInterface","GetBestInterface function [IP Helper]","_iphlp_getbestinterface","iphlp.getbestinterface","iphlpapi/GetBestInterface"]
old-location: iphlp\getbestinterface.htm
tech.root: IpHlp
ms.assetid: 9171cdf7-4057-4a8d-a34c-1b7b1f94bcb1
ms.date: 12/05/2018
ms.keywords: GetBestInterface, GetBestInterface function [IP Helper], _iphlp_getbestinterface, iphlp.getbestinterface, iphlpapi/GetBestInterface
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
 - GetBestInterface
 - iphlpapi/GetBestInterface
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
 - GetBestInterface
---

# GetBestInterface function


## -description

The 
<b>GetBestInterface</b> function retrieves the index of the interface that has the best route to the specified IPv4 address.

## -parameters

### -param dwDestAddr [in]

The destination IPv4 address for which to retrieve the interface that has the best route, in the form of an <a href="/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a> structure.

### -param pdwBestIfIndex [out]

A pointer to a <b>DWORD</b> variable that receives the index of the interface that has the best route to the IPv4 address specified by <i>dwDestAddr</i>.

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
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>pdwBestIfIndex</i> parameter or if the <i>pdwBestIfIndex</i> points to memory that cannot be written.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer.

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

The <b>GetBestInterface</b> function only works with IPv4 addresses. For use with IPv6 addresses, the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestinterfaceex">GetBestInterfaceEx</a> must be used. 

For information about the <b>IPAddr</b> data type, see 
<a href="/windows/desktop/WinProg/windows-data-types">Windows Data Types</a>. To convert an IP address between dotted decimal notation and <b>IPAddr</b> format, use the 
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a> and 
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a> functions.

On Windows Vista and later, the <i>pdwBestIfIndex</i> parameter is treated internally by IP Helper as a pointer to a <b>NET_IFINDEX</b> datatype.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestinterfaceex">GetBestInterfaceEx</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getbestroute">GetBestRoute</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a>



<a href="/windows/desktop/api/iprtrmib/ns-iprtrmib-mib_best_if">MIB_BEST_IF</a>



<a href="/windows/desktop/WinProg/windows-data-types">Windows Data Types</a>