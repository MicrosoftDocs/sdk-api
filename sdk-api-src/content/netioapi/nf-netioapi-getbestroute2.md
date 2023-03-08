---
UID: NF:netioapi.GetBestRoute2
title: GetBestRoute2 function (netioapi.h)
description: Retrieves the IP route entry on the local computer for the best route to the specified destination IP address.
helpviewer_keywords: ["GetBestRoute2","GetBestRoute2 function [IP Helper]","iphlp.getbestroute2","netioapi/GetBestRoute2"]
old-location: iphlp\getbestroute2.htm
tech.root: IpHlp
ms.assetid: 7bc16824-c98f-4cd5-a589-e198b48b637c
ms.date: 12/05/2018
ms.keywords: GetBestRoute2, GetBestRoute2 function [IP Helper], iphlp.getbestroute2, netioapi/GetBestRoute2
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - GetBestRoute2
 - netioapi/GetBestRoute2
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
 - GetBestRoute2
---

# GetBestRoute2 function


## -description

The 
<b>GetBestRoute2</b> function  retrieves the IP route entry on the local computer for the best route to the specified destination IP address.

## -parameters

### -param InterfaceLuid [in, optional]

The locally unique identifier (LUID) to specify the network interface associated with an IP route entry.

### -param InterfaceIndex [in]

The local index value to specify the network interface associated with an IP route entry. This index value may change when a network adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.

### -param SourceAddress [in]

The source IP address. This parameter may be omitted and passed as a <b>NULL</b> pointer.

### -param DestinationAddress [in]

The destination IP address.

### -param AddressSortOptions [in]

A set of options that affect how IP addresses are sorted. This parameter is not currently used.

### -param BestRoute [out]

A pointer to the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a> for the best route from the source IP address to the destination IP address.

### -param BestSourceAddress [out]

A pointer to the best source IP address.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>DestinationAddress</i>,  <i>BestSourceAddress</i>, or the <i>BestRoute</i> parameter. This error is also returned if the  <i>DestinationAddress</i> parameter does not specify an IPv4 or IPv6 address and family.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified interface could not be found. This error is returned if the  network interface specified by the <i>InterfaceLuid</i> or <i>InterfaceIndex</i> parameter could not be found.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer and an IPv4 address and family  was specified in the <i>DestinationAddress</i>  parameter. This error is also returned if no IPv6 stack is on the local computer and an IPv6 address and family  was specified in the <i>DestinationAddress</i>  parameter. 

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

The <b>GetBestRoute2</b> function is defined on Windows Vista and later. 

The <b>GetBestRoute2</b> function is used to retrieve a <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a> structure entry for the best route from a source IP address to a destination IP address.  

On input, the <i>DestinationAddress</i> parameter must be initialized to a valid IPv4 or IPv6 address and family. On input, the <i>SourceAddress</i> parameter may be initialized to the preferred IPv4 or IPv6 address and family. In addition, at least one of the following parameters must be initialized: the <i>InterfaceLuid</i> or <i>InterfaceIndex</i>.

The parameters are used in the order listed above. So if the <i>InterfaceLuid</i> is specified, then this member is used to determine the interface. If no value was set for the  <i>InterfaceLuid</i> member (the values of this member was set to zero), then the <i>InterfaceIndex</i> member is next used to determine the interface. 

On output when the call is successful, <b>GetBestRoute2</b> retrieves and <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a> structure for the best route from the source IP address the destination IP address.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-createipforwardentry2">CreateIpForwardEntry2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-deleteipforwardentry2">DeleteIpForwardEntry2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipforwardentry2">GetIpForwardEntry2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipforwardtable2">GetIpForwardTable2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-initializeipforwardentry">InitializeIpForwardEntry</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_row2">MIB_IPFORWARD_ROW2</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipforward_table2">MIB_IPFORWARD_TABLE2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyroutechange2">NotifyRouteChange2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-setipforwardentry2">SetIpForwardEntry2</a>