---
UID: NF:iphlpapi.GetAdaptersAddresses
title: GetAdaptersAddresses function (iphlpapi.h)
description: Retrieves the addresses associated with the adapters on the local computer.
old-location: iphlp\getadaptersaddresses.htm
tech.root: IpHlp
ms.assetid: 7b34138f-7263-4b73-95df-9e854fd81135
ms.date: 12/05/2018
ms.keywords: AF_INET, AF_INET6, AF_UNSPEC, GAA_FLAG_INCLUDE_ALL_COMPARTMENTS, GAA_FLAG_INCLUDE_ALL_INTERFACES, GAA_FLAG_INCLUDE_GATEWAYS, GAA_FLAG_INCLUDE_PREFIX, GAA_FLAG_INCLUDE_TUNNEL_BINDINGORDER, GAA_FLAG_INCLUDE_WINS_INFO, GAA_FLAG_SKIP_ANYCAST, GAA_FLAG_SKIP_DNS_SERVER, GAA_FLAG_SKIP_FRIENDLY_NAME, GAA_FLAG_SKIP_MULTICAST, GAA_FLAG_SKIP_UNICAST, GetAdaptersAddresses, GetAdaptersAddresses function [IP Helper], _iphlp_getadaptersaddresses, iphlp.getadaptersaddresses, iphlpapi/GetAdaptersAddresses
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
 - GetAdaptersAddresses
 - iphlpapi/GetAdaptersAddresses
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
 - GetAdaptersAddresses
---

# GetAdaptersAddresses function


## -description

The 
<b>GetAdaptersAddresses</b> function retrieves the addresses associated with the adapters on the local computer.

## -parameters

### -param Family [in]

The address family of the addresses to retrieve. This parameter must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_UNSPEC"></a><a id="af_unspec"></a><dl>
<dt><b>AF_UNSPEC</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Return both IPv4 and IPv6 addresses associated with adapters with IPv4 or IPv6 enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Return only IPv4 addresses associated with adapters with IPv4 enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
Return only IPv6 addresses associated with adapters with IPv6 enabled.

</td>
</tr>
</table>

### -param Flags [in]

The type of addresses to retrieve. The possible values are defined in the <i>Iptypes.h</i> header file. Note that the <i>Iptypes.h</i> header file is automatically included in <i>Iphlpapi.h</i>, and should never be used directly.

This parameter is a combination of the following values. If this parameter is zero, then unicast, anycast, and multicast IP addresses will be returned.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GAA_FLAG_SKIP_UNICAST"></a><a id="gaa_flag_skip_unicast"></a><dl>
<dt><b>GAA_FLAG_SKIP_UNICAST</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
Do not return unicast addresses.

</td>
</tr>
<tr>
<td width="40%"><a id="GAA_FLAG_SKIP_ANYCAST"></a><a id="gaa_flag_skip_anycast"></a><dl>
<dt><b>GAA_FLAG_SKIP_ANYCAST</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Do not return IPv6 anycast addresses.

</td>
</tr>
<tr>
<td width="40%"><a id="GAA_FLAG_SKIP_MULTICAST"></a><a id="gaa_flag_skip_multicast"></a><dl>
<dt><b>GAA_FLAG_SKIP_MULTICAST</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
Do not return multicast addresses.

</td>
</tr>
<tr>
<td width="40%"><a id="GAA_FLAG_SKIP_DNS_SERVER"></a><a id="gaa_flag_skip_dns_server"></a><dl>
<dt><b>GAA_FLAG_SKIP_DNS_SERVER</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
Do not return addresses of DNS servers.

</td>
</tr>
<tr>
<td width="40%"><a id="GAA_FLAG_INCLUDE_PREFIX"></a><a id="gaa_flag_include_prefix"></a><dl>
<dt><b>GAA_FLAG_INCLUDE_PREFIX</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
Return a list of IP address prefixes on this adapter. When this flag is set, IP address prefixes are returned for both IPv6 and IPv4 addresses. 

This flag is supported on Windows XP with SP1 and later.

</td>
</tr>
<tr>
<td width="40%"><a id="GAA_FLAG_SKIP_FRIENDLY_NAME"></a><a id="gaa_flag_skip_friendly_name"></a><dl>
<dt><b>GAA_FLAG_SKIP_FRIENDLY_NAME</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
Do not return the adapter friendly name.

</td>
</tr>
<tr>
<td width="40%"><a id="GAA_FLAG_INCLUDE_WINS_INFO"></a><a id="gaa_flag_include_wins_info"></a><dl>
<dt><b>GAA_FLAG_INCLUDE_WINS_INFO</b></dt>
<dt>0x0040</dt>
</dl>
</td>
<td width="60%">
Return addresses of Windows Internet Name Service (WINS) servers. 

This flag is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="GAA_FLAG_INCLUDE_GATEWAYS"></a><a id="gaa_flag_include_gateways"></a><dl>
<dt><b>GAA_FLAG_INCLUDE_GATEWAYS</b></dt>
<dt>0x0080</dt>
</dl>
</td>
<td width="60%">
Return the addresses of default gateways. 

This flag is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="GAA_FLAG_INCLUDE_ALL_INTERFACES"></a><a id="gaa_flag_include_all_interfaces"></a><dl>
<dt><b>GAA_FLAG_INCLUDE_ALL_INTERFACES</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Return addresses for all NDIS interfaces. 

This flag is supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="GAA_FLAG_INCLUDE_ALL_COMPARTMENTS"></a><a id="gaa_flag_include_all_compartments"></a><dl>
<dt><b>GAA_FLAG_INCLUDE_ALL_COMPARTMENTS</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Return addresses in all routing compartments. 

This flag is not currently supported and reserved for future use.

</td>
</tr>
<tr>
<td width="40%"><a id="GAA_FLAG_INCLUDE_TUNNEL_BINDINGORDER"></a><a id="gaa_flag_include_tunnel_bindingorder"></a><dl>
<dt><b>GAA_FLAG_INCLUDE_TUNNEL_BINDINGORDER</b></dt>
<dt>0x0400</dt>
</dl>
</td>
<td width="60%">
Return the adapter addresses sorted in tunnel binding order. This flag is supported on Windows Vista and later.

</td>
</tr>
</table>

### -param Reserved [in]

This parameter is not currently used, but is reserved for future system use. The calling application should pass <b>NULL</b> for this parameter.

### -param AdapterAddresses [in, out]

A pointer to a buffer that contains a linked list of <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a> structures on successful return.

### -param SizePointer [in, out]

A pointer to a variable that specifies the size of the buffer pointed to by <i>AdapterAddresses</i>.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b> (defined to the same value as <b>NO_ERROR</b>).

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ADDRESS_NOT_ASSOCIATED</b></dt>
</dl>
</td>
<td width="60%">
An address has not yet been associated with the network endpoint. DHCP lease information was available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The buffer size indicated by the <i>SizePointer</i> parameter is too small to hold the adapter information or the <i>AdapterAddresses</i> parameter is <b>NULL</b>. The <i>SizePointer</i> parameter returned points to the required size of the buffer to hold the adapter information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid. This error is returned for any of the following conditions: the <i>SizePointer</i> parameter is <b>NULL</b>, the <i>Address</i> parameter is not <b>AF_INET</b>, <b>AF_INET6</b>, or <b>AF_UNSPEC</b>, or the address information for the parameters requested is greater than <b>ULONG_MAX</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory resources are available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_DATA</b></dt>
</dl>
</td>
<td width="60%">
No addresses were found for the requested parameters.

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

The  
<b>GetAdaptersAddresses</b> function can retrieve information for IPv4 and IPv6 addresses. 

Addresses are returned as a linked list of <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a> structures in the buffer pointed to by the <i>AdapterAddresses</i> parameter. The application that calls the <b>GetAdaptersAddresses</b> function must allocate the amount of memory needed to return the <b>IP_ADAPTER_ADDRESSES</b> structures pointed to by the <i>AdapterAddresses</i> parameter. When these returned structures are no longer required, the application should free the memory allocated. This can be accomplished by calling the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a> function to allocate memory and later calling the <a href="/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a> function to free the allocated memory, as shown in the example code. Other memory allocation and free functions can be used as long as the same family of functions are used for both the allocation and the free function.

<b>GetAdaptersAddresses</b> is implemented only as a synchronous function call.  The <b>GetAdaptersAddresses</b> function requires a significant amount of network resources and time to complete since all of the low-level network interface tables must be traversed. 

One method that can be used to determine the memory needed to return the <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a> structures pointed to by the <i>AdapterAddresses</i> parameter is to pass too small a buffer size as indicated in the <i>SizePointer</i> parameter in the first call to the <b>GetAdaptersAddresses</b> function,  so the function will fail with <b>ERROR_BUFFER_OVERFLOW</b>. When the return value is <b>ERROR_BUFFER_OVERFLOW</b>, the <i>SizePointer</i> parameter returned points to the required size of the buffer to hold the adapter information. Note that it is possible for the buffer size required for the <b>IP_ADAPTER_ADDRESSES</b> structures pointed to by the <i>AdapterAddresses</i> parameter to change between subsequent calls to the <b>GetAdaptersAddresses</b> function if an adapter address is added or removed.   However, this method of using the <b>GetAdaptersAddresses</b> function is strongly discouraged. This method requires calling the <b>GetAdaptersAddresses</b> function multiple times. 

The recommended method of calling the <b>GetAdaptersAddresses</b> function is to pre-allocate a 15KB working buffer pointed to by the <i>AdapterAddresses</i> parameter. On typical computers, this dramatically reduces the chances that the <b>GetAdaptersAddresses</b> function returns <b>ERROR_BUFFER_OVERFLOW</b>, which would require calling  <b>GetAdaptersAddresses</b> function multiple times. The example code illustrates this method of use. 

In versions prior to Windows 10, the order in which adapters appear in the list returned by this function can be controlled from the Network Connections folder: select the Advanced Settings menu item from the Advanced menu. Starting with Windows 10, the order in which adapters appear in the list is determined by the IPv4 or IPv6 route metric.

If the GAA_FLAG_INCLUDE_ALL_INTERFACES is set, then all NDIS adapters will be retrieved even those addresses associated with adapters not bound to an address family specified in the <i>Family</i> parameter. When this flag is not set, then only the addresses that are bound to an adapter enabled for the address family specified in the <i>Family</i> parameter are returned.

The size of the <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a> structure was changed on Windows XP with Service Pack 1 (SP1) and later. Several additional members were added to this structure. The size of the <b>IP_ADAPTER_ADDRESSES</b> structure was also changed on Windows Vista and later. A number of additional members were added to this structure. The size of the 
     <b>IP_ADAPTER_ADDRESSES</b> structure also changed on 
     Windows Vista with Service Pack 1 (SP1)and later and onWindows Server 2008 and later. One additional member was added to this structure. The <b>Length</b> member of the <b>IP_ADAPTER_ADDRESSES</b> structure returned in the linked list of structures in the buffer pointed to by the <i>AdapterAddresses</i> parameter should be used to determine which version of the <b>IP_ADAPTER_ADDRESSES</b> structure is being used. 

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipaddrtable">GetIpAddrTable</a> function retrieves the interface–to–IPv4 address mapping table on a local computer and returns this information in an <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipaddrtable">MIB_IPADDRTABLE</a> structure.

On the Platform Software Development Kit (SDK) released for Windows Server 2003 and earlier, the return value for the <b>GetAdaptersAddresses</b> function was defined as a <b>DWORD</b>, rather than a <b>ULONG</b>.

The <a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a> structure is used in the <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a> structure pointed to by the <i>AdapterAddresses</i> parameter. On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>SOCKET_ADDRESS</b> structure is defined in the <i>Ws2def.h</i> header file which is automatically included by the <i>Winsock2.h</i> header file. On the Platform SDK released for Windows Server 2003 and Windows XP, the <b>SOCKET_ADDRESS</b> structure is declared in the <i>Winsock2.h</i> header file. In order to use the <b>IP_ADAPTER_ADDRESSES</b> structure, the <i>Winsock2.h</i> header file must be included before the <i>Iphlpapi.h</i> header file.  


#### Examples

This example retrieves the <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a> structure for the adapters associated with the system and prints some members  for each adapter interface.


```cpp
#include <winsock2.h>
#include <iphlpapi.h>
#include <stdio.h>
#include <stdlib.h>

// Link with Iphlpapi.lib
#pragma comment(lib, "IPHLPAPI.lib")

#define WORKING_BUFFER_SIZE 15000
#define MAX_TRIES 3

#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x))
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))

/* Note: could also use malloc() and free() */

int __cdecl main(int argc, char **argv)
{

    /* Declare and initialize variables */

    DWORD dwRetVal = 0;

    unsigned int i = 0;

    // Set the flags to pass to GetAdaptersAddresses
    ULONG flags = GAA_FLAG_INCLUDE_PREFIX;

    // default to unspecified address family (both)
    ULONG family = AF_UNSPEC;

    LPVOID lpMsgBuf = NULL;

    PIP_ADAPTER_ADDRESSES pAddresses = NULL;
    ULONG outBufLen = 0;
    ULONG Iterations = 0;

    PIP_ADAPTER_ADDRESSES pCurrAddresses = NULL;
    PIP_ADAPTER_UNICAST_ADDRESS pUnicast = NULL;
    PIP_ADAPTER_ANYCAST_ADDRESS pAnycast = NULL;
    PIP_ADAPTER_MULTICAST_ADDRESS pMulticast = NULL;
    IP_ADAPTER_DNS_SERVER_ADDRESS *pDnServer = NULL;
    IP_ADAPTER_PREFIX *pPrefix = NULL;

    if (argc != 2) {
        printf(" Usage: getadapteraddresses family\n");
        printf("        getadapteraddresses 4 (for IPv4)\n");
        printf("        getadapteraddresses 6 (for IPv6)\n");
        printf("        getadapteraddresses A (for both IPv4 and IPv6)\n");
        exit(1);
    }

    if (atoi(argv[1]) == 4)
        family = AF_INET;
    else if (atoi(argv[1]) == 6)
        family = AF_INET6;

    printf("Calling GetAdaptersAddresses function with family = ");
    if (family == AF_INET)
        printf("AF_INET\n");
    if (family == AF_INET6)
        printf("AF_INET6\n");
    if (family == AF_UNSPEC)
        printf("AF_UNSPEC\n\n");

    // Allocate a 15 KB buffer to start with.
    outBufLen = WORKING_BUFFER_SIZE;

    do {

        pAddresses = (IP_ADAPTER_ADDRESSES *) MALLOC(outBufLen);
        if (pAddresses == NULL) {
            printf
                ("Memory allocation failed for IP_ADAPTER_ADDRESSES struct\n");
            exit(1);
        }

        dwRetVal =
            GetAdaptersAddresses(family, flags, NULL, pAddresses, &outBufLen);

        if (dwRetVal == ERROR_BUFFER_OVERFLOW) {
            FREE(pAddresses);
            pAddresses = NULL;
        } else {
            break;
        }

        Iterations++;

    } while ((dwRetVal == ERROR_BUFFER_OVERFLOW) && (Iterations < MAX_TRIES));

    if (dwRetVal == NO_ERROR) {
        // If successful, output some information from the data we received
        pCurrAddresses = pAddresses;
        while (pCurrAddresses) {
            printf("\tLength of the IP_ADAPTER_ADDRESS struct: %ld\n",
                   pCurrAddresses->Length);
            printf("\tIfIndex (IPv4 interface): %u\n", pCurrAddresses->IfIndex);
            printf("\tAdapter name: %s\n", pCurrAddresses->AdapterName);

            pUnicast = pCurrAddresses->FirstUnicastAddress;
            if (pUnicast != NULL) {
                for (i = 0; pUnicast != NULL; i++)
                    pUnicast = pUnicast->Next;
                printf("\tNumber of Unicast Addresses: %d\n", i);
            } else
                printf("\tNo Unicast Addresses\n");

            pAnycast = pCurrAddresses->FirstAnycastAddress;
            if (pAnycast) {
                for (i = 0; pAnycast != NULL; i++)
                    pAnycast = pAnycast->Next;
                printf("\tNumber of Anycast Addresses: %d\n", i);
            } else
                printf("\tNo Anycast Addresses\n");

            pMulticast = pCurrAddresses->FirstMulticastAddress;
            if (pMulticast) {
                for (i = 0; pMulticast != NULL; i++)
                    pMulticast = pMulticast->Next;
                printf("\tNumber of Multicast Addresses: %d\n", i);
            } else
                printf("\tNo Multicast Addresses\n");

            pDnServer = pCurrAddresses->FirstDnsServerAddress;
            if (pDnServer) {
                for (i = 0; pDnServer != NULL; i++)
                    pDnServer = pDnServer->Next;
                printf("\tNumber of DNS Server Addresses: %d\n", i);
            } else
                printf("\tNo DNS Server Addresses\n");

            printf("\tDNS Suffix: %wS\n", pCurrAddresses->DnsSuffix);
            printf("\tDescription: %wS\n", pCurrAddresses->Description);
            printf("\tFriendly name: %wS\n", pCurrAddresses->FriendlyName);

            if (pCurrAddresses->PhysicalAddressLength != 0) {
                printf("\tPhysical address: ");
                for (i = 0; i < (int) pCurrAddresses->PhysicalAddressLength;
                     i++) {
                    if (i == (pCurrAddresses->PhysicalAddressLength - 1))
                        printf("%.2X\n",
                               (int) pCurrAddresses->PhysicalAddress[i]);
                    else
                        printf("%.2X-",
                               (int) pCurrAddresses->PhysicalAddress[i]);
                }
            }
            printf("\tFlags: %ld\n", pCurrAddresses->Flags);
            printf("\tMtu: %lu\n", pCurrAddresses->Mtu);
            printf("\tIfType: %ld\n", pCurrAddresses->IfType);
            printf("\tOperStatus: %ld\n", pCurrAddresses->OperStatus);
            printf("\tIpv6IfIndex (IPv6 interface): %u\n",
                   pCurrAddresses->Ipv6IfIndex);
            printf("\tZoneIndices (hex): ");
            for (i = 0; i < 16; i++)
                printf("%lx ", pCurrAddresses->ZoneIndices[i]);
            printf("\n");

            printf("\tTransmit link speed: %I64u\n", pCurrAddresses->TransmitLinkSpeed);
            printf("\tReceive link speed: %I64u\n", pCurrAddresses->ReceiveLinkSpeed);

            pPrefix = pCurrAddresses->FirstPrefix;
            if (pPrefix) {
                for (i = 0; pPrefix != NULL; i++)
                    pPrefix = pPrefix->Next;
                printf("\tNumber of IP Adapter Prefix entries: %d\n", i);
            } else
                printf("\tNumber of IP Adapter Prefix entries: 0\n");

            printf("\n");

            pCurrAddresses = pCurrAddresses->Next;
        }
    } else {
        printf("Call to GetAdaptersAddresses failed with error: %d\n",
               dwRetVal);
        if (dwRetVal == ERROR_NO_DATA)
            printf("\tNo addresses were found for the requested parameters\n");
        else {

            if (FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER |
                    FORMAT_MESSAGE_FROM_SYSTEM | FORMAT_MESSAGE_IGNORE_INSERTS, 
                    NULL, dwRetVal, MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),   
                    // Default language
                    (LPTSTR) & lpMsgBuf, 0, NULL)) {
                printf("\tError: %s", lpMsgBuf);
                LocalFree(lpMsgBuf);
                if (pAddresses)
                    FREE(pAddresses);
                exit(1);
            }
        }
    }

    if (pAddresses) {
        FREE(pAddresses);
    }

    return 0;
}

```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipaddrtable">GetIpAddrTable</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-heapalloc">HeapAlloc</a>



<a href="/windows/desktop/api/heapapi/nf-heapapi-heapfree">HeapFree</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_lh">IP_ADAPTER_ADDRESSES</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipaddrtable">MIB_IPADDRTABLE</a>



<a href="/windows/desktop/api/ws2def/ns-ws2def-socket_address">SOCKET_ADDRESS</a>



<a href="/windows/desktop/WinSock/windows-sockets-start-page-2">Windows Sockets</a>