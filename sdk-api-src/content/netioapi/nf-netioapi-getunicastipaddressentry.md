---
UID: NF:netioapi.GetUnicastIpAddressEntry
title: GetUnicastIpAddressEntry function (netioapi.h)
description: Retrieves information for an existing unicast IP address entry on the local computer.
helpviewer_keywords: ["GetUnicastIpAddressEntry","GetUnicastIpAddressEntry function [IP Helper]","iphlp.getunicastipaddressentry","netioapi/GetUnicastIpAddressEntry"]
old-location: iphlp\getunicastipaddressentry.htm
tech.root: IpHlp
ms.assetid: d5475c09-05dd-41d7-80ff-63c52d78468c
ms.date: 12/05/2018
ms.keywords: GetUnicastIpAddressEntry, GetUnicastIpAddressEntry function [IP Helper], iphlp.getunicastipaddressentry, netioapi/GetUnicastIpAddressEntry
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
 - GetUnicastIpAddressEntry
 - netioapi/GetUnicastIpAddressEntry
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
 - GetUnicastIpAddressEntry
---

# GetUnicastIpAddressEntry function


## -description

The 
<b>GetUnicastIpAddressEntry</b> function  retrieves information for an existing unicast IP address entry on the local computer.

## -parameters

### -param Row [in, out]

A pointer to a 
<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure entry for a unicast IP address entry. On successful return, this structure will be updated with the properties for an existing unicast IP address.

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
The system cannot find the file specified. This error is returned if the  network interface LUID or interface index specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter is not a value on the local machine.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is incorrect. This error is returned if a <b>NULL</b> pointer is passed in the <i>Row</i> parameter, the <b>Address</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> pointed to by the <i>Row</i> parameter is not set to a valid unicast IPv4 or IPv6 address, or both the <b>InterfaceLuid</b> and <b>InterfaceIndex</b> members of the <b>MIB_UNICASTIPADDRESS_ROW</b> pointed to by the <i>Row</i> parameter are unspecified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Element not found. This error is returned if the  network interface specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure pointed to by the <i>Row</i> parameter does not match the IP address specified in the <b>Address</b> member in the <b>MIB_UNICASTIPADDRESS_ROW</b> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer and an IPv4 address is specified in the <b>Address</b> member of the  <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure pointed to by the <i>Row</i> parameter. This error is also returned if no IPv6 stack is on the local computer and an IPv6 address is specified in the <b>Address</b> member. 

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

The <b>GetUnicastIpAddressEntry</b> function is defined on Windows Vista and later. 

The <b>GetUnicastIpAddressEntry</b> function is normally used to retrieve an existing <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure entry to be modified.  An application can then change the members in the <b>MIB_UNICASTIPADDRESS_ROW</b> entry it wishes to modify, and then call the <a href="/windows/desktop/api/netioapi/nf-netioapi-createunicastipaddressentry">SetUnicastIpAddressEntry</a> function. 

On input, the <b>Address</b> member in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure pointed to by the <i>Row</i> parameter must be initialized to a valid unicast IPv4 or IPv6 address. The <b>si_family</b> member of the <b>SOCKADDR_INET</b> structure  in the  <b>Address</b> member must be initialized to either <b>AF_INET</b> or <b>AF_INET6</b> and the related <b>Ipv4</b> or <b>Ipv6</b> member of the  <b>SOCKADDR_INET</b> structure must be set to a valid unicast IP address. In addition, at least one of the following members in the <b>MIB_UNICASTIPADDRESS_ROW</b> structure pointed to the <i>Row</i> parameter must be initialized: the <b>InterfaceLuid</b> or <b>InterfaceIndex</b>.

The fields are used in the order listed above. So if the <b>InterfaceLuid</b> is specified, then this member is used to determine the interface. If no value is set for the  <b>InterfaceLuid</b> member (the value of this member is set to zero), then the <b>InterfaceIndex</b> member is next used to determine the interface. 

On output when the call is successful, <b>GetUnicastIpAddressEntry</b> retrieves the other properties for the unicast IP address and fills out the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure pointed to by the <i>Row</i> parameter. 

The <a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddresstable">GetUnicastIpAddressTable</a> function can be called to enumerate the unicast IP address entries on a local computer.


#### Examples

The following example retrieves a unicast IP address entry specified on the command line and prints some values from the retrieved <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structure.


```cpp

#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h.>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <ws2ipdef.h>
#include <iphlpapi.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Iphlpapi.lib and Ws2_32.lib
#pragma comment (lib, "iphlpapi.lib")
#pragma comment (lib, "Ws2_32.lib")

void PrintUnicastIpAddress(PMIB_UNICASTIPADDRESS_ROW pIpRow);

int __cdecl wmain(int argc, WCHAR **argv)
{

    // Declare and initialize variables

    ULONG Result = 0;
    ULONG ifIndex;

    // default to unspecified address family
    ULONG addressFamily = AF_UNSPEC;

    IN_ADDR Ipv4Addr;
    IN6_ADDR Ipv6Addr;

    MIB_UNICASTIPADDRESS_ROW ipRow = {0};
    
    // Validate the parameters
    if (argc < 4) {
        wprintf(L"usage: %s <AddressFamily> <IPAddress> <InterfaceIndex>\n", argv[0]);
        wprintf(L"   Gets the UnicastIpAddressEntry for an AddressFamily,\n");
        wprintf(L"     Interface Index, and IP address\n");
        wprintf(L"   Examples\n");
        wprintf(L"     Get the IPv4 loopback at interface index=1\n");
        wprintf(L"       %s 4 127.0.0.1 1\n", argv[0]);
        wprintf(L"     Get the IPv6 loopback at interface index=1\n");
        wprintf(L"       %s 6 ::1 1\n", argv[0]);
        exit(1);
    }

    if (_wtoi(argv[1]) == 4) {
        addressFamily = AF_INET;
        if (InetPtonW(addressFamily, argv[2], &Ipv4Addr) != 1) {
            wprintf(L"Unable to parse IPv4 address string: %s\n", argv[3]);
            exit(1);
        }
    } else if (_wtoi(argv[1]) == 6) {
        addressFamily = AF_INET6;
        if (InetPton(addressFamily, argv[2], &Ipv6Addr) != 1) {
            wprintf(L"Unable to parse IPv6 address string: %s\n", argv[3]);
            exit(1);
        }
    }

    ifIndex = _wtoi(argv[3]);

    ipRow.Address.si_family = (ADDRESS_FAMILY) addressFamily;
    ipRow.InterfaceIndex = ifIndex;

    if (addressFamily == AF_INET) {
        ipRow.Address.si_family = AF_INET;
        memcpy(&ipRow.Address.Ipv4.sin_addr, &Ipv4Addr, sizeof (IN_ADDR));
    }
    if (addressFamily == AF_INET6) {
        ipRow.Address.si_family = AF_INET6;
        memcpy(&ipRow.Address.Ipv6.sin6_addr, &Ipv6Addr, sizeof (IN6_ADDR));
    }

    Result = GetUnicastIpAddressEntry(&ipRow);
    if (Result != NO_ERROR) {
        wprintf(L"GetUnicastIpAddressEntry returned error: %lu\n", Result);
        exit(1);
    }
    PrintUnicastIpAddress(&ipRow);
    
    exit(0);
}

void PrintUnicastIpAddress(PMIB_UNICASTIPADDRESS_ROW pipRow)
{

    WCHAR Ipv4String[16] = { 0 };
    WCHAR Ipv6String[46] = { 0 };

    // Print some variables from the rows in the table
    wprintf(L"AddressFamily:\t\t\t ");
    switch (pipRow->Address.si_family) {
    case AF_INET:
        wprintf(L"IPv4\n");
        if (InetNtop(AF_INET, &pipRow->Address.Ipv4.sin_addr, Ipv4String, 16) !=
            NULL)
            wprintf(L"IPv4 Address:\t\t\t %ws\n", Ipv4String);
        break;
    case AF_INET6:
        wprintf(L"IPv6\n");
        if (InetNtop(AF_INET6, &pipRow->Address.Ipv6.sin6_addr, Ipv6String, 46)
            != NULL)
            wprintf(L"IPv6 Address:\t\t\t %s\n", Ipv6String);
        break;
    default:
        wprintf(L"Other: %d\n", pipRow->Address.si_family);
        break;
    }

    wprintf(L"Interface LUID NetLuidIndex:\t %lu\n",
           pipRow->InterfaceLuid.Info.NetLuidIndex);
    wprintf(L"Interface LUID IfType:\t\t ");
    switch (pipRow->InterfaceLuid.Info.IfType) {
    case IF_TYPE_OTHER:
        wprintf(L"Other\n");
        break;
    case IF_TYPE_ETHERNET_CSMACD:
        wprintf(L"Ethernet\n");
        break;
    case IF_TYPE_ISO88025_TOKENRING:
        wprintf(L"Token ring\n");
        break;
    case IF_TYPE_PPP:
        wprintf(L"PPP\n");
        break;
    case IF_TYPE_SOFTWARE_LOOPBACK:
        wprintf(L"Software loopback\n");
        break;
    case IF_TYPE_ATM:
        wprintf(L"ATM\n");
        break;
    case IF_TYPE_IEEE80211:
        wprintf(L"802.11 wireless\n");
        break;
    case IF_TYPE_TUNNEL:
        wprintf(L"Tunnel encapsulation\n");
        break;
    case IF_TYPE_IEEE1394:
        wprintf(L"IEEE 1394 (Firewire)\n");
        break;
    default:
        wprintf(L"Unknown: %d\n", pipRow->InterfaceLuid.Info.IfType);
        break;
    }

    wprintf(L"Interface Index:\t\t %lu\n", pipRow->InterfaceIndex);

    wprintf(L"Prefix Origin:\t\t\t ");
    switch (pipRow->PrefixOrigin) {
    case IpPrefixOriginOther:
        wprintf(L"IpPrefixOriginOther\n");
        break;
    case IpPrefixOriginManual:
        wprintf(L"IpPrefixOriginManual\n");
        break;
    case IpPrefixOriginWellKnown:
        wprintf(L"IpPrefixOriginWellKnown\n");
        break;
    case IpPrefixOriginDhcp:
        wprintf(L"IpPrefixOriginDhcp\n");
        break;
    case IpPrefixOriginRouterAdvertisement:
        wprintf(L"IpPrefixOriginRouterAdvertisement\n");
        break;
    case IpPrefixOriginUnchanged:
        wprintf(L"IpPrefixOriginUnchanged\n");
        break;
    default:
        wprintf(L"Unknown: %d\n", pipRow->PrefixOrigin);
        break;
    }

    wprintf(L"Suffix Origin:\t\t\t ");
    switch (pipRow->SuffixOrigin) {
    case IpSuffixOriginOther:
        wprintf(L"IpSuffixOriginOther\n");
        break;
    case IpSuffixOriginManual:
        wprintf(L"IpSuffixOriginManual\n");
        break;
    case IpSuffixOriginWellKnown:
        wprintf(L"IpSuffixOriginWellKnown\n");
        break;
    case IpSuffixOriginDhcp:
        wprintf(L"IpSuffixOriginDhcp\n");
        break;
    case IpSuffixOriginLinkLayerAddress:
        wprintf(L"IpSuffixOriginLinkLayerAddress\n");
        break;
    case IpSuffixOriginRandom:
        wprintf(L"IpSuffixOriginRandom\n");
        break;
    case IpSuffixOriginUnchanged:
        wprintf(L"IpSuffixOriginUnchanged\n");
        break;
    default:
        wprintf(L"Unknown: %d\n", pipRow->SuffixOrigin);
        break;
    }

    wprintf(L"Valid Lifetime:\t\t\t 0x%x (%u)\n",
           pipRow->ValidLifetime, pipRow->ValidLifetime);

    wprintf(L"Preferred Lifetime:\t\t 0x%x (%u)\n",
           pipRow->PreferredLifetime, pipRow->PreferredLifetime);

    wprintf(L"OnLink PrefixLength:\t\t %lu\n", pipRow->OnLinkPrefixLength);

    wprintf(L"Skip As Source:\t\t\t ");
    if (pipRow->SkipAsSource)
        wprintf(L"Yes\n");
    else
        wprintf(L"No\n");

    wprintf(L"Dad State:\t\t\t ");
    switch (pipRow->DadState) {
    case IpDadStateInvalid:
        wprintf(L"IpDadStateInvalid\n");
        break;
    case IpDadStateTentative:
        wprintf(L"IpDadStateTentative\n");
        break;
    case IpDadStateDuplicate:
        wprintf(L"IpDadStateDuplicate\n");
        break;
    case IpDadStateDeprecated:
        wprintf(L"IpDadStateDeprecated\n");
        break;
    case IpDadStatePreferred:
        wprintf(L"IpDadStatePreferred\n");
        break;
    default:
        wprintf(L"Unknown: %d\n", pipRow->DadState);
        break;
    }

    wprintf(L"\n");
}


```

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-createunicastipaddressentry">CreateUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-deleteunicastipaddressentry">DeleteUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddresstable">GetUnicastIpAddressTable</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-initializeunicastipaddressentry">InitializeUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_table">MIB_UNICASTIPADDRESS_TABLE</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyunicastipaddresschange">NotifyUnicastIpAddressChange</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-setunicastipaddressentry">SetUnicastIpAddressEntry</a>