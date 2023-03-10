---
UID: NF:netioapi.CreateSortedAddressPairs
title: CreateSortedAddressPairs function (netioapi.h)
description: Takes a supplied list of potential IP destination addresses, pairs the destination addresses with the host machine's local IP addresses, and sorts the pairs according to which address pair is best suited for communication between the two peers.
helpviewer_keywords: ["CreateSortedAddressPairs","CreateSortedAddressPairs function [IP Helper]","iphlp.createsortedaddresspairs","netioapi/CreateSortedAddressPairs"]
old-location: iphlp\createsortedaddresspairs.htm
tech.root: IpHlp
ms.assetid: cdc90d63-15a4-4278-afc3-dbf9ad6ba698
ms.date: 12/05/2018
ms.keywords: CreateSortedAddressPairs, CreateSortedAddressPairs function [IP Helper], iphlp.createsortedaddresspairs, netioapi/CreateSortedAddressPairs
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateSortedAddressPairs
 - netioapi/CreateSortedAddressPairs
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
 - CreateSortedAddressPairs
---

# CreateSortedAddressPairs function


## -description

The 
<b>CreateSortedAddressPairs</b> function  takes a supplied list of potential IP destination addresses, pairs the destination addresses with the host machine's local IP addresses, and sorts the pairs according to which address
    pair is best suited for communication between the two peers.

## -parameters

### -param SourceAddressList [in, optional]

Must be <b>NULL</b>. Reserved for future use.

### -param SourceAddressCount [in]

Must be 0. Reserved for future use.

### -param DestinationAddressList [in]

A pointer to an array of <a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR_IN6</a> structures that contain a list of potential IPv6 destination addresses.
        Any IPv4 addresses must be represented in the IPv4-mapped IPv6 address format which enables an IPv6 only application to communicate with an IPv4 node.

### -param DestinationAddressCount [in]

The number of destination addresses pointed to by the <i>DestinationAddressList</i> parameter.

### -param AddressSortOptions [in]

Reserved for future use.

### -param SortedAddressPairList [out]

A pointer to store an array of <a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-sockaddr_in6_pair">SOCKADDR_IN6_PAIR</a> structures that contain a list of pairs of IPv6 addresses
        sorted in the preferred order of communication, if the function call is successful.

### -param SortedAddressPairCount [out]

A pointer to store the number of address pairs pointed to by the <i>SortedAddressPairList</i> parameter, if the function call is successful.

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
An invalid parameter was passed to the function. This error is returned if the <i>DestinationAddressList</i>, <i>SortedAddressPairList</i>, or  <i>SortedAddressPairCount</i> parameters <b>NULL</b>,  or the <i>DestinationAddressCount</i> was greater than 500. This error is also returned if the <i>SourceAddressList</i> is not <b>NULL</b> or the <i>SourceAddressPairCount</i> parameter is not zero. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough storage is available to process this command. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv6 stack is on the local computer.

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

The <b>CreateSortedAddressPairs</b> function is defined on Windows Vista and later. 

The <b>CreateSortedAddressPairs</b> function takes a list of source and destination IPv6 addresses, and returns a list of
    pairs of addresses in sorted order.  The list is sorted by which address
    pair is best suited for communication between the source and destination address. 

The list of source addresses pointed to by the <i>SourceAddressList</i> is currently reserved for future and must be a <b>NULL</b> pointer. The <i>SourceAddressCount</i> is currently reserved for future and must be zero. The <b>CreateSortedAddressPairs</b> function currently  uses all of the host machine's local addresses for the source address list.


The list of destination addresses is pointed to by the <i>DestinationAddressList</i> parameter. The list of destination addresses is an array of <a href="/windows/desktop/WinSock/sockaddr-2">SOCKADDR_IN6</a> structures.  Any IPv4 addresses must be represented in the IPv4-mapped IPv6 address format which enables an IPv6 only application to communicate with an IPv4 node. For more information on the IPv4-mapped IPv6 address format, see <a href="/windows/desktop/WinSock/dual-stack-sockets">Dual-Stack Sockets</a>. The <i>DestinationAddressCount</i> parameter contains the number of destination addresses pointed to by the <i>DestinationAddressList</i> parameter. The <b>CreateSortedAddressPairs</b> function supports a maximum of 500 destination addresses.

If the <b>CreateSortedAddressPairs</b> function is successful, the <i>SortedAddressPairList</i> parameter points to an array of <a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-sockaddr_in6_pair">SOCKADDR_IN6_PAIR</a> structures that contain the sorted address pairs. When this returned list is no longer required, free the memory used by the list by calling the <a href="/windows/desktop/api/netioapi/nf-netioapi-freemibtable">FreeMibTable</a> function.

## -see-also

<a href="/windows/desktop/WinSock/dual-stack-sockets">Dual-Stack Sockets</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-freemibtable">FreeMibTable</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-sockaddr_in6_pair">SOCKADDR_IN6_PAIR</a>



<a href="/windows/desktop/WinSock/using-sio-address-list-sort">Using SIO_ADDRESS_LIST_SORT</a>



<a href="/windows/desktop/WinSock/sockaddr-2">sockaddr</a>