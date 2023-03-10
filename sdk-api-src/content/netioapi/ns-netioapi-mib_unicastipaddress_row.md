---
UID: NS:netioapi._MIB_UNICASTIPADDRESS_ROW
title: MIB_UNICASTIPADDRESS_ROW (netioapi.h)
description: Stores information about a unicast IP address.
helpviewer_keywords: ["*PMIB_UNICASTIPADDRESS_ROW","IpDadStateDeprecated","IpDadStateDuplicate","IpDadStateInvalid","IpDadStatePreferred","IpDadStateTentative","IpPrefixOriginDhcp","IpPrefixOriginManual","IpPrefixOriginOther","IpPrefixOriginRouterAdvertisement","IpPrefixOriginUnchanged","IpPrefixOriginWellKnown","IpSuffixOriginDhcp","IpSuffixOriginLinkLayerAddress","IpSuffixOriginManual","IpSuffixOriginOther","IpSuffixOriginRandom","IpSuffixOriginUnchanged","IpSuffixOriginWellKnown","MIB_UNICASTIPADDRESS_ROW","MIB_UNICASTIPADDRESS_ROW structure [MIB]","PMIB_UNICASTIPADDRESS_ROW","PMIB_UNICASTIPADDRESS_ROW structure pointer [MIB]","_MIB_UNICASTIPADDRESS_ROW","mib.mib_unicastipaddress_row","netioapi/MIB_UNICASTIPADDRESS_ROW","netioapi/PMIB_UNICASTIPADDRESS_ROW"]
old-location: mib\mib_unicastipaddress_row.htm
tech.root: MIB
ms.assetid: f329bafd-9e83-4754-a9a9-e7e111229c90
ms.date: 12/05/2018
ms.keywords: '*PMIB_UNICASTIPADDRESS_ROW, IpDadStateDeprecated, IpDadStateDuplicate, IpDadStateInvalid, IpDadStatePreferred, IpDadStateTentative, IpPrefixOriginDhcp, IpPrefixOriginManual, IpPrefixOriginOther, IpPrefixOriginRouterAdvertisement, IpPrefixOriginUnchanged, IpPrefixOriginWellKnown, IpSuffixOriginDhcp, IpSuffixOriginLinkLayerAddress, IpSuffixOriginManual, IpSuffixOriginOther, IpSuffixOriginRandom, IpSuffixOriginUnchanged, IpSuffixOriginWellKnown, MIB_UNICASTIPADDRESS_ROW, MIB_UNICASTIPADDRESS_ROW structure [MIB], PMIB_UNICASTIPADDRESS_ROW, PMIB_UNICASTIPADDRESS_ROW structure pointer [MIB], _MIB_UNICASTIPADDRESS_ROW, mib.mib_unicastipaddress_row, netioapi/MIB_UNICASTIPADDRESS_ROW, netioapi/PMIB_UNICASTIPADDRESS_ROW'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: MIB_UNICASTIPADDRESS_ROW, *PMIB_UNICASTIPADDRESS_ROW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MIB_UNICASTIPADDRESS_ROW
 - netioapi/_MIB_UNICASTIPADDRESS_ROW
 - PMIB_UNICASTIPADDRESS_ROW
 - netioapi/PMIB_UNICASTIPADDRESS_ROW
 - MIB_UNICASTIPADDRESS_ROW
 - netioapi/MIB_UNICASTIPADDRESS_ROW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Netioapi.h
api_name:
 - MIB_UNICASTIPADDRESS_ROW
---

# MIB_UNICASTIPADDRESS_ROW structure


## -description

The 
<b>MIB_UNICASTIPADDRESS_ROW</b> structure stores information about a unicast IP address.

## -struct-fields

### -field Address

Type: <b><a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-sockaddr_inet">SOCKADDR_INET</a></b>

The unicast IP address. This member can be an IPv6 address or an IPv4 address.

### -field InterfaceLuid

Type: <b>NET_LUID</b>

The locally unique identifier (LUID) for the network interface associated with this IP address.

### -field InterfaceIndex

Type: <b>NET_IFINDEX</b>

The local index value for the network interface associated with this IP address. This index value may change when a network adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.

### -field PrefixOrigin

Type: <b>NL_PREFIX_ORIGIN</b>

The origin of the prefix or network part of IP the address. This member can be one of the values from the <b>NL_PREFIX_ORIGIN</b> enumeration type defined in the <i>Nldef.h</i> header file. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IpPrefixOriginOther"></a><a id="ipprefixoriginother"></a><a id="IPPREFIXORIGINOTHER"></a><dl>
<dt><b>IpPrefixOriginOther</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The IP address prefix was configured using a source other than those defined in this enumeration. This value is applicable to an IPv6 or IPv4 address.

</td>
</tr>
<tr>
<td width="40%"><a id="IpPrefixOriginManual"></a><a id="ipprefixoriginmanual"></a><a id="IPPREFIXORIGINMANUAL"></a><dl>
<dt><b>IpPrefixOriginManual</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The IP address prefix was configured manually. This value is applicable to an IPv6 or IPv4 address.

</td>
</tr>
<tr>
<td width="40%"><a id="IpPrefixOriginWellKnown"></a><a id="ipprefixoriginwellknown"></a><a id="IPPREFIXORIGINWELLKNOWN"></a><dl>
<dt><b>IpPrefixOriginWellKnown</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The IP address prefix was configured using a well-known address. This value is applicable to an IPv6 link-local address or an IPv6 loopback address.

</td>
</tr>
<tr>
<td width="40%"><a id="IpPrefixOriginDhcp"></a><a id="ipprefixorigindhcp"></a><a id="IPPREFIXORIGINDHCP"></a><dl>
<dt><b>IpPrefixOriginDhcp</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The IP address prefix was configured using DHCP. This value is applicable to an IPv4 address  configured using DHCP or an IPv6 address configured using DHCPv6.

</td>
</tr>
<tr>
<td width="40%"><a id="IpPrefixOriginRouterAdvertisement"></a><a id="ipprefixoriginrouteradvertisement"></a><a id="IPPREFIXORIGINROUTERADVERTISEMENT"></a><dl>
<dt><b>IpPrefixOriginRouterAdvertisement</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The IP address prefix was configured using router advertisement. This value is applicable to an anonymous IPv6 address that was generated after receiving a router advertisement.

</td>
</tr>
<tr>
<td width="40%"><a id="IpPrefixOriginUnchanged"></a><a id="ipprefixoriginunchanged"></a><a id="IPPREFIXORIGINUNCHANGED"></a><dl>
<dt><b>IpPrefixOriginUnchanged</b></dt>
<dt>16</dt>
</dl>
</td>
<td width="60%">
The IP address prefix should be unchanged. This value is used when setting the properties for a unicast  IP interface when the value for the IP prefix origin should be unchanged.

</td>
</tr>
</table>

### -field SuffixOrigin

Type: <b>NL_SUFFIX_ORIGIN</b>

The origin of the suffix or host part of IP the address. This member can be one of the values from the <b>NL_SUFFIX_ORIGIN</b> enumeration type defined in the <i>Nldef.h</i> header file. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IpSuffixOriginOther"></a><a id="ipsuffixoriginother"></a><a id="IPSUFFIXORIGINOTHER"></a><dl>
<dt><b>IpSuffixOriginOther</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The IP address suffix was configured using a source other than those defined in this enumeration. This value is applicable to an IPv6 or IPv4 address.

</td>
</tr>
<tr>
<td width="40%"><a id="IpSuffixOriginManual"></a><a id="ipsuffixoriginmanual"></a><a id="IPSUFFIXORIGINMANUAL"></a><dl>
<dt><b>IpSuffixOriginManual</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The IP address suffix was configured manually. This value is applicable to an IPv6 or IPv4 address.

</td>
</tr>
<tr>
<td width="40%"><a id="IpSuffixOriginWellKnown"></a><a id="ipsuffixoriginwellknown"></a><a id="IPSUFFIXORIGINWELLKNOWN"></a><dl>
<dt><b>IpSuffixOriginWellKnown</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The IP address suffix was configured using a well-known address. This value is applicable to an IPv6 link-local address or an IPv6 loopback address.

</td>
</tr>
<tr>
<td width="40%"><a id="IpSuffixOriginDhcp"></a><a id="ipsuffixorigindhcp"></a><a id="IPSUFFIXORIGINDHCP"></a><dl>
<dt><b>IpSuffixOriginDhcp</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The IP address suffix was configured using DHCP. This value is applicable to an IPv4 address configured using DHCP or an IPv6 address configured using DHCPv6.

</td>
</tr>
<tr>
<td width="40%"><a id="IpSuffixOriginLinkLayerAddress"></a><a id="ipsuffixoriginlinklayeraddress"></a><a id="IPSUFFIXORIGINLINKLAYERADDRESS"></a><dl>
<dt><b>IpSuffixOriginLinkLayerAddress</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The IP address suffix was the link local address. This value is applicable to an IPv6 link-local address or an IPv6 address where the network part was generated based on a router advertisement and the host part was based on the MAC hardware address.

</td>
</tr>
<tr>
<td width="40%"><a id="IpSuffixOriginRandom"></a><a id="ipsuffixoriginrandom"></a><a id="IPSUFFIXORIGINRANDOM"></a><dl>
<dt><b>IpSuffixOriginRandom</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The IP address suffix was generated randomly. This value is applicable to an anonymous IPv6 address where the host part of the address was generated randomly from the MAC hardware address after receiving a router advertisement.

</td>
</tr>
<tr>
<td width="40%"><a id="IpSuffixOriginUnchanged"></a><a id="ipsuffixoriginunchanged"></a><a id="IPSUFFIXORIGINUNCHANGED"></a><dl>
<dt><b>IpSuffixOriginUnchanged</b></dt>
<dt>16</dt>
</dl>
</td>
<td width="60%">
The IP address suffix should be unchanged. This value is used when setting the properties for a unicast  IP interface when the value for the IP suffix origin should be unchanged.

</td>
</tr>
</table>

### -field ValidLifetime

Type: <b>ULONG</b>

The maximum time, in seconds, that the IP address is valid. A value of 0xffffffff  is considered to be infinite.

### -field PreferredLifetime

Type: <b>ULONG</b>

The preferred time, in seconds, that the IP address is valid. A value of 0xffffffff is considered to be infinite.

### -field OnLinkPrefixLength

Type: <b>UINT8</b>

The length, in bits, of the prefix or network part of the IP address. For a unicast IPv4 address, any  value greater than 32 is an illegal value. For a unicast IPv6 address, any  value greater than 128 is an illegal value. A value of 255 is commonly used to represent an illegal value.

### -field SkipAsSource

Type: <b>BOOLEAN</b>

This member specifies if the address can be used as an IP source address.

### -field DadState

Type: <b>NL_DAD_STATE</b>

The duplicate Address detection (DAD) state. Duplicate address detection is applicable to both IPv6 and IPv4 addresses. This member can be one of the values from the <b>NL_DAD_STATE</b> enumeration type defined in the <i>Nldef.h</i> header file. 


<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IpDadStateInvalid"></a><a id="ipdadstateinvalid"></a><a id="IPDADSTATEINVALID"></a><dl>
<dt><b>IpDadStateInvalid</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The DAD state is invalid. 

</td>
</tr>
<tr>
<td width="40%"><a id="IpDadStateTentative"></a><a id="ipdadstatetentative"></a><a id="IPDADSTATETENTATIVE"></a><dl>
<dt><b>IpDadStateTentative</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The DAD state is tentative. 

</td>
</tr>
<tr>
<td width="40%"><a id="IpDadStateDuplicate"></a><a id="ipdadstateduplicate"></a><a id="IPDADSTATEDUPLICATE"></a><dl>
<dt><b>IpDadStateDuplicate</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
A duplicate IP address has been detected. 

</td>
</tr>
<tr>
<td width="40%"><a id="IpDadStateDeprecated"></a><a id="ipdadstatedeprecated"></a><a id="IPDADSTATEDEPRECATED"></a><dl>
<dt><b>IpDadStateDeprecated</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The IP address has been deprecated.

</td>
</tr>
<tr>
<td width="40%"><a id="IpDadStatePreferred"></a><a id="ipdadstatepreferred"></a><a id="IPDADSTATEPREFERRED"></a><dl>
<dt><b>IpDadStatePreferred</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The IP address is the preferred address. 

</td>
</tr>
</table>

### -field ScopeId

Type: <b>SCOPE_ID</b>

The scope ID of the IP address. This member is applicable only to an IPv6 address. This member cannot be set. It is automatically determined by the interface on which the address was added.

### -field CreationTimeStamp

Type: <b>LARGE_INTEGER</b>

The time stamp when the IP address was created.

## -remarks

The <b>MIB_UNICASTIPADDRESS_ROW</b> structure is defined on Windows Vista and later. 

The <b>SkipAsSource</b> member of the <b>MIB_UNICASTIPADDRESS_ROW</b> structure affects the operation of the <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>, <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>, and <a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a> functions in Windows sockets. If the <i>pNodeName</i> parameter passed to the <b>getaddrinfo</b> or <b>GetAddrInfoW</b> functions or the <i>pName</i> parameter passed to the <b>GetAddrInfoEx</b> function points to a computer name, all permanent addresses for the computer that can be used as a source address are returned. On Windows Vista and later, these addresses would include all unicast IP addresses returned by the  <a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddresstable">GetUnicastIpAddressTable</a> or <a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddressentry">GetUnicastIpAddressEntry</a> functions in which the <b>SkipAsSource</b> member is set to false in the <b>MIB_UNICASTIPADDRESS_ROW</b> structure. 

If the <i>pNodeName</i> or <i>pName</i> parameter refers to a cluster virtual server name, only virtual server addresses are returned. On Windows Vista and later, these addresses would include all unicast IP addresses returned by the  <a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddresstable">GetUnicastIpAddressTable</a> or <a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddressentry">GetUnicastIpAddressEntry</a> functions in which the <b>SkipAsSource</b> member is set to true in the <b>MIB_UNICASTIPADDRESS_ROW</b> structure. See <a href="/previous-versions/windows/desktop/mscs/windows-clustering">Windows Clustering</a> for more information about clustering.

Windows 7 with Service Pack 1 (SP1) and Windows Server 2008 R2 with Service Pack 1 (SP1) add support to Netsh.exe for setting the SkipAsSource attribute on an IP address. This hotfix also changes the behavior such that if the <b>SkipAsSource</b> member in the <b>MIB_UNICASTIPADDRESS_ROW</b> structure is set to false, the IP address will be registered in DNS. If the <b>SkipAsSource</b> member is set to true, the IP address is not registered in DNS.  

A hotfix is available for Windows 7 and Windows Server 2008 R2 that adds support to Netsh.exe for setting the SkipAsSource attribute on an IP address.  This hotfix also changes the behavior such that if the <b>SkipAsSource</b> member in the <b>MIB_UNICASTIPADDRESS_ROW</b> structure is set to false, the IP address will be registered in DNS. If the <b>SkipAsSource</b> member is set to true, the IP address is not registered in DNS.  For more information, see Knowledge Base (KB) <a href="https://support.microsoft.com/kb/2386184">2386184</a>.   

A similar hotfix is also available for Windows Vista with Service Pack 2 (SP2) and Windows Server 2008 with Service Pack 2 (SP2) that adds support to Netsh.exe for setting the SkipAsSource attribute on an IP address. This hotfix also changes behavior such that if the <b>SkipAsSource</b> member in the <b>MIB_UNICASTIPADDRESS_ROW</b> structure is set to false, the IP address will be registered in DNS. If the <b>SkipAsSource</b> member is set to true, the IP address is not registered in DNS.


#### Examples

The following example retrieves a unicast IP address table and prints some values from each of the retrieved <b>MIB_UNICASTIPADDRESS_ROW</b> structures.


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

int __cdecl wmain()
{

    // Declare and initialize variables

    unsigned int i;

    DWORD Result = 0;

    WCHAR Ipv4String[16] = { 0 };
    WCHAR Ipv6String[46] = { 0 };

    PMIB_UNICASTIPADDRESS_TABLE pipTable = NULL;

    Result = GetUnicastIpAddressTable(AF_UNSPEC, &pipTable);
    if (Result != NO_ERROR) {
        wprintf(L"GetUnicastIpAddressTable returned error: %ld\n", Result);
        exit(1);
    }
    // Print some variables from the rows in the table
    wprintf(L"Number of table entries: %d\n\n", pipTable->NumEntries);

    for (i = 0; i < pipTable->NumEntries; i++) {
        wprintf(L"AddressFamily[%d]:\t\t ", i);

        switch (pipTable->Table[i].Address.si_family) {
        case AF_INET:
            wprintf(L"IPv4\n");
            if (InetNtopW
                (AF_INET, &pipTable->Table[i].Address.Ipv4.sin_addr, Ipv4String,
                 16) != NULL)
                wprintf(L"IPv4 Address:\t\t\t %ws\n", Ipv4String);
            break;
        case AF_INET6:
            wprintf(L"IPv6\n");
            if (InetNtopW
                (AF_INET6, &pipTable->Table[i].Address.Ipv6.sin6_addr,
                 Ipv6String, 46) != NULL)
                wprintf(L"IPv6 Address:\t\t\t %ws\n", Ipv6String);
            break;
        default:
            wprintf(L"Other: %d\n", pipTable->Table[i].Address.si_family);
            break;
        }

        wprintf(L"Interface LUID NetLuidIndex[%d]:  %lu\n",
               i, pipTable->Table[i].InterfaceLuid.Info.NetLuidIndex);
        wprintf(L"Interface LUID IfType[%d]:\t ", i);
        switch (pipTable->Table[i].InterfaceLuid.Info.IfType) {
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
            wprintf(L"Unknown: %d\n",
                   pipTable->Table[i].InterfaceLuid.Info.IfType);
            break;
        }

        wprintf(L"Interface Index[%d]:\t\t %lu\n",
               i, pipTable->Table[i].InterfaceIndex);

        wprintf(L"Prefix Origin[%d]:\t\t ", i);
        switch (pipTable->Table[i].PrefixOrigin) {
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
            wprintf(L"Unknown: %d\n", pipTable->Table[i].PrefixOrigin);
            break;
        }

        wprintf(L"Suffix Origin[%d]:\t\t ", i);
        switch (pipTable->Table[i].SuffixOrigin) {
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
            wprintf(L"Unknown: %d\n", pipTable->Table[i].SuffixOrigin);
            break;
        }

        wprintf(L"Valid Lifetime[%d]:\t\t 0x%x (%u)\n", i,
               pipTable->Table[i].ValidLifetime,
               pipTable->Table[i].ValidLifetime);

        wprintf(L"Preferred Lifetime[%d]:\t\t 0x%x (%u)\n", i,
               pipTable->Table[i].PreferredLifetime,
               pipTable->Table[i].PreferredLifetime);

        wprintf(L"OnLink PrefixLength[%d]:\t\t %lu\n", i,
               pipTable->Table[i].OnLinkPrefixLength);

        wprintf(L"Skip As Source[%d]:\t\t ", i);
        if (pipTable->Table[i].SkipAsSource)
            wprintf(L"Yes\n");
        else
            wprintf(L"No\n");

        wprintf(L"Dad State[%d]:\t\t\t ", i);
        switch (pipTable->Table[i].DadState) {
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
            wprintf(L"Unknown: %d\n", pipTable->Table[i].DadState);
            break;
        }

        wprintf(L"\n");
    }

    if (pipTable != NULL) {
        FreeMibTable(pipTable);
        pipTable = NULL;
    }

    exit(0);
}


```

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-createunicastipaddressentry">CreateUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-deleteunicastipaddressentry">DeleteUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfoexa">GetAddrInfoEx</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfow">GetAddrInfoW</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddressentry">GetUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddresstable">GetUnicastIpAddressTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-initializeunicastipaddressentry">InitializeUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_table">MIB_UNICASTIPADDRESS_TABLE</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-sockaddr_inet">SOCKADDR_INET</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-setunicastipaddressentry">SetUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo">getaddrinfo</a>