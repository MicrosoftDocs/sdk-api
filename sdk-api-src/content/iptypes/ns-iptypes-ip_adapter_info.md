---
UID: NS:iptypes._IP_ADAPTER_INFO
title: IP_ADAPTER_INFO (iptypes.h)
description: Contains information about a particular network adapter on the local computer.
helpviewer_keywords: ["*PIP_ADAPTER_INFO","IF_TYPE_IEEE80211","IF_TYPE_ISO88025_TOKENRING","IP_ADAPTER_INFO","IP_ADAPTER_INFO structure [IP Helper]","MIB_IF_TYPE_ETHERNET","MIB_IF_TYPE_LOOPBACK","MIB_IF_TYPE_OTHER","MIB_IF_TYPE_PPP","MIB_IF_TYPE_SLIP","PIP_ADAPTER_INFO","PIP_ADAPTER_INFO structure pointer [IP Helper]","_iphlp_ip_adapter_info","iphlp.ip_adapter_info","iptypes/IP_ADAPTER_INFO","iptypes/PIP_ADAPTER_INFO"]
old-location: iphlp\ip_adapter_info.htm
tech.root: IpHlp
ms.assetid: f8035801-ca0c-4d86-bfc5-8e2d746af1b4
ms.date: 12/05/2018
ms.keywords: '*PIP_ADAPTER_INFO, IF_TYPE_IEEE80211, IF_TYPE_ISO88025_TOKENRING, IP_ADAPTER_INFO, IP_ADAPTER_INFO structure [IP Helper], MIB_IF_TYPE_ETHERNET, MIB_IF_TYPE_LOOPBACK, MIB_IF_TYPE_OTHER, MIB_IF_TYPE_PPP, MIB_IF_TYPE_SLIP, PIP_ADAPTER_INFO, PIP_ADAPTER_INFO structure pointer [IP Helper], _iphlp_ip_adapter_info, iphlp.ip_adapter_info, iptypes/IP_ADAPTER_INFO, iptypes/PIP_ADAPTER_INFO'
req.header: iptypes.h
req.include-header: Iphlpapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IP_ADAPTER_INFO, *PIP_ADAPTER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _IP_ADAPTER_INFO
 - iptypes/_IP_ADAPTER_INFO
 - PIP_ADAPTER_INFO
 - iptypes/PIP_ADAPTER_INFO
 - IP_ADAPTER_INFO
 - iptypes/IP_ADAPTER_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iptypes.h
api_name:
 - IP_ADAPTER_INFO
---

# IP_ADAPTER_INFO structure


## -description

The 
<b>IP_ADAPTER_INFO</b> structure contains information about a particular network adapter on the local computer.

## -struct-fields

### -field Next

Type: <b>struct _IP_ADAPTER_INFO*</b>

A pointer to the next adapter in the list of adapters.

### -field ComboIndex

Type: <b>DWORD</b>

Reserved.

### -field AdapterName

Type: <b>char[MAX_ADAPTER_NAME_LENGTH + 4]</b>

An ANSI character string of the name of the adapter.

### -field Description

Type: <b>char[MAX_ADAPTER_DESCRIPTION_LENGTH + 4]</b>

An ANSI character string that contains the description of the adapter.

### -field AddressLength

Type: <b>UINT</b>

The length, in bytes,  of the hardware address for the adapter.

### -field Address

Type: <b>BYTE[MAX_ADAPTER_ADDRESS_LENGTH]</b>

The hardware address for the adapter represented as a <b>BYTE</b> array.

### -field Index

Type: <b>DWORD</b>

The adapter index. 

The adapter index  may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.

### -field Type

Type: <b>UINT</b>

The adapter type. Possible values for the adapter type are listed in the <i>Ipifcons.h</i> header file.


The table below lists common values for the adapter type although other values are possible on Windows Vista and later. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MIB_IF_TYPE_OTHER"></a><a id="mib_if_type_other"></a><dl>
<dt><b>MIB_IF_TYPE_OTHER</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Some other type of network interface.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IF_TYPE_ETHERNET"></a><a id="mib_if_type_ethernet"></a><dl>
<dt><b>MIB_IF_TYPE_ETHERNET</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
An Ethernet network interface.

</td>
</tr>
<tr>
<td width="40%"><a id="IF_TYPE_ISO88025_TOKENRING"></a><a id="if_type_iso88025_tokenring"></a><dl>
<dt><b>IF_TYPE_ISO88025_TOKENRING</b></dt>
<dt>9</dt>
</dl>
</td>
<td width="60%">
MIB_IF_TYPE_TOKENRING

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IF_TYPE_PPP"></a><a id="mib_if_type_ppp"></a><dl>
<dt><b>MIB_IF_TYPE_PPP</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
A PPP network interface.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IF_TYPE_LOOPBACK"></a><a id="mib_if_type_loopback"></a><dl>
<dt><b>MIB_IF_TYPE_LOOPBACK</b></dt>
<dt>24</dt>
</dl>
</td>
<td width="60%">
A software loopback network interface.

</td>
</tr>
<tr>
<td width="40%"><a id="MIB_IF_TYPE_SLIP"></a><a id="mib_if_type_slip"></a><dl>
<dt><b>MIB_IF_TYPE_SLIP</b></dt>
<dt>28</dt>
</dl>
</td>
<td width="60%">
An ATM network interface.

</td>
</tr>
<tr>
<td width="40%"><a id="IF_TYPE_IEEE80211"></a><a id="if_type_ieee80211"></a><dl>
<dt><b>IF_TYPE_IEEE80211</b></dt>
<dt>71</dt>
</dl>
</td>
<td width="60%">
An IEEE 802.11 wireless network interface.

<div class="alert"><b>Note</b>  This adapter type is returned on Windows Vista and later.  On Windows Server 2003 and Windows XP , an IEEE 802.11 wireless network interface returns an adapter type of  <b>MIB_IF_TYPE_ETHERNET</b>.</div>
<div> </div>
</td>
</tr>
</table>

### -field DhcpEnabled

Type: <b>UINT</b>

An option value  that specifies whether the dynamic host configuration protocol (DHCP) is enabled for this adapter.

### -field CurrentIpAddress

Type: <b>PIP_ADDR_STRING</b>

Reserved.

### -field IpAddressList

Type: <b>IP_ADDR_STRING</b>

The list of IPv4 addresses associated with this adapter represented as  a linked list of <b>IP_ADDR_STRING</b> structures. An adapter can have multiple IPv4 addresses assigned to it.

### -field GatewayList

Type: <b>IP_ADDR_STRING</b>

The IPv4 address of the gateway for this adapter represented as  a linked list of <b>IP_ADDR_STRING</b> structures. An adapter can have multiple IPv4 gateway addresses assigned to it. This list usually contains a single entry for IPv4 address of the default gateway for this adapter.

### -field DhcpServer

Type: <b>IP_ADDR_STRING</b>

The IPv4 address of the DHCP server for this adapter represented as  a linked list of <b>IP_ADDR_STRING</b> structures. This  list contains a single entry for the IPv4 address of the DHCP server for this adapter. A value of 255.255.255.255 indicates the DHCP server could not be reached, or is in the process of being reached. 

This member is only valid when the <b>DhcpEnabled</b> member is nonzero.

### -field HaveWins

Type: <b>BOOL</b>

An option value that specifies whether this adapter uses the Windows Internet Name Service (WINS).

### -field PrimaryWinsServer

Type: <b>IP_ADDR_STRING</b>

The IPv4 address of the primary WINS server represented as  a linked list of <b>IP_ADDR_STRING</b> structures. This list contains a single entry for the IPv4 address of the primary WINS server for this adapter. 

This member is only valid when the <b>HaveWins</b> member is <b>TRUE</b>.

### -field SecondaryWinsServer

Type: <b>IP_ADDR_STRING</b>

The IPv4 address of the secondary WINS server represented as  a linked list of <b>IP_ADDR_STRING</b> structures. An adapter can have multiple secondary WINS server addresses assigned to it. 

This member is only valid when the <b>HaveWins</b> member is <b>TRUE</b>.

### -field LeaseObtained

Type: <b>time_t</b>

The time when the current DHCP lease was obtained. 

This member is only valid when the <b>DhcpEnabled</b> member is nonzero.

### -field LeaseExpires

Type: <b>time_t</b>

The time when the current DHCP lease expires. 

This member is only valid when the <b>DhcpEnabled</b> member is nonzero.

## -remarks

The 
<b>IP_ADAPTER_INFO</b> structure is limited to IPv4 information about a particular network adapter on the local computer. The 
<b>IP_ADAPTER_INFO</b> structure is retrieved by calling the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersinfo">GetAdaptersInfo</a> function.

When using Visual Studio 2005 and later, the <b>time_t</b> datatype defaults to an 8-byte datatype, not the 4-byte datatype used for the <b>LeaseObtained</b> and <b>LeaseExpires</b> members on a 32-bit platform. To properly use the <b>IP_ADAPTER_INFO</b> structure on a 32-bit platform, define <b>_USE_32BIT_TIME_T</b> (use <code>-D _USE_32BIT_TIME_T</code> as an option, for example) when compiling the application to force the <b>time_t</b> datatype to a 4-byte datatype.

For use on Windows XP and later, the <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a> structure contains both IPv4 and IPv6 information. The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a> function retrieves IPv4 and IPv6 adapter information. 


#### Examples

This example retrieves the adapter information and prints various properties of each adapter.


```cpp
#include <winsock2.h>
#include <iphlpapi.h>
#include <stdio.h>
#include <stdlib.h>
#pragma comment(lib, "IPHLPAPI.lib")

#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x))
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))

/* Note: could also use malloc() and free() */

int __cdecl main()
{

    /* Declare and initialize variables */

// It is possible for an adapter to have multiple
// IPv4 addresses, gateways, and secondary WINS servers
// assigned to the adapter. 
//
// Note that this sample code only prints out the 
// first entry for the IP address/mask, and gateway, and
// the primary and secondary WINS server for each adapter. 

    PIP_ADAPTER_INFO pAdapterInfo;
    PIP_ADAPTER_INFO pAdapter = NULL;
    DWORD dwRetVal = 0;
    UINT i;

/* variables used to print DHCP time info */
    struct tm newtime;
    char buffer[32];
    errno_t error;

    ULONG ulOutBufLen = sizeof (IP_ADAPTER_INFO);
    pAdapterInfo = (IP_ADAPTER_INFO *) MALLOC(sizeof (IP_ADAPTER_INFO));
    if (pAdapterInfo == NULL) {
        printf("Error allocating memory needed to call GetAdaptersinfo\n");
        return 1;
    }
// Make an initial call to GetAdaptersInfo to get
// the necessary size into the ulOutBufLen variable
    if (GetAdaptersInfo(pAdapterInfo, &ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
        FREE(pAdapterInfo);
        pAdapterInfo = (IP_ADAPTER_INFO *) MALLOC(ulOutBufLen);
        if (pAdapterInfo == NULL) {
            printf("Error allocating memory needed to call GetAdaptersinfo\n");
            return 1;
        }
    }

    if ((dwRetVal = GetAdaptersInfo(pAdapterInfo, &ulOutBufLen)) == NO_ERROR) {
        pAdapter = pAdapterInfo;
        while (pAdapter) {
            printf("\tComboIndex: \t%d\n", pAdapter->ComboIndex);
            printf("\tAdapter Name: \t%s\n", pAdapter->AdapterName);
            printf("\tAdapter Desc: \t%s\n", pAdapter->Description);
            printf("\tAdapter Addr: \t");
            for (i = 0; i < pAdapter->AddressLength; i++) {
                if (i == (pAdapter->AddressLength - 1))
                    printf("%.2X\n", (int) pAdapter->Address[i]);
                else
                    printf("%.2X-", (int) pAdapter->Address[i]);
            }
            printf("\tIndex: \t%d\n", pAdapter->Index);
            printf("\tType: \t");
            switch (pAdapter->Type) {
            case MIB_IF_TYPE_OTHER:
                printf("Other\n");
                break;
            case MIB_IF_TYPE_ETHERNET:
                printf("Ethernet\n");
                break;
            case MIB_IF_TYPE_TOKENRING:
                printf("Token Ring\n");
                break;
            case MIB_IF_TYPE_FDDI:
                printf("FDDI\n");
                break;
            case MIB_IF_TYPE_PPP:
                printf("PPP\n");
                break;
            case MIB_IF_TYPE_LOOPBACK:
                printf("Lookback\n");
                break;
            case MIB_IF_TYPE_SLIP:
                printf("Slip\n");
                break;
            default:
                printf("Unknown type %ld\n", pAdapter->Type);
                break;
            }

            printf("\tIP Address: \t%s\n",
                   pAdapter->IpAddressList.IpAddress.String);
            printf("\tIP Mask: \t%s\n", pAdapter->IpAddressList.IpMask.String);

            printf("\tGateway: \t%s\n", pAdapter->GatewayList.IpAddress.String);
            printf("\t***\n");

            if (pAdapter->DhcpEnabled) {
                printf("\tDHCP Enabled: Yes\n");
                printf("\t  DHCP Server: \t%s\n",
                       pAdapter->DhcpServer.IpAddress.String);

                printf("\t  Lease Obtained: ");
                /* Display local time */
                error = _localtime32_s(&newtime, (__time32_t*) &pAdapter->LeaseObtained);
                if (error)
                    printf("Invalid Argument to _localtime32_s\n");
                else {
                    // Convert to an ASCII representation 
                    error = asctime_s(buffer, 32, &newtime);
                    if (error)
                        printf("Invalid Argument to asctime_s\n");
                    else
                        /* asctime_s returns the string terminated by \n\0 */
                        printf("%s", buffer);
                }

                printf("\t  Lease Expires:  ");
                error = _localtime32_s(&newtime, (__time32_t*) &pAdapter->LeaseExpires);
                if (error)
                    printf("Invalid Argument to _localtime32_s\n");
                else {
                    // Convert to an ASCII representation 
                    error = asctime_s(buffer, 32, &newtime);
                    if (error)
                        printf("Invalid Argument to asctime_s\n");
                    else
                        /* asctime_s returns the string terminated by \n\0 */
                        printf("%s", buffer);
                }
            } else
                printf("\tDHCP Enabled: No\n");

            if (pAdapter->HaveWins) {
                printf("\tHave Wins: Yes\n");
                printf("\t  Primary Wins Server:    %s\n",
                       pAdapter->PrimaryWinsServer.IpAddress.String);
                printf("\t  Secondary Wins Server:  %s\n",
                       pAdapter->SecondaryWinsServer.IpAddress.String);
            } else
                printf("\tHave Wins: No\n");
            pAdapter = pAdapter->Next;
            printf("\n");
        }
    } else {
        printf("GetAdaptersInfo failed with error: %d\n", dwRetVal);

    }
    if (pAdapterInfo)
        FREE(pAdapterInfo);

    return 0;
}

```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersinfo">GetAdaptersInfo</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/IpHlp/ip-helper-structures">IP Helper Structures</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_address_string">IP_ADDRESS_STRING</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_addr_string">IP_ADDR_STRING</a>
