---
UID: NF:netioapi.GetUnicastIpAddressTable
title: GetUnicastIpAddressTable function (netioapi.h)
description: Retrieves the unicast IP address table on the local computer.
helpviewer_keywords: ["AF_INET","AF_INET6","AF_UNSPEC","GetUnicastIpAddressTable","GetUnicastIpAddressTable function [IP Helper]","iphlp.getunicastipaddresstable","netioapi/GetUnicastIpAddressTable"]
old-location: iphlp\getunicastipaddresstable.htm
tech.root: IpHlp
ms.assetid: bdafc4a4-5f3c-4dd5-ba9b-4f6045a82652
ms.date: 12/05/2018
ms.keywords: AF_INET, AF_INET6, AF_UNSPEC, GetUnicastIpAddressTable, GetUnicastIpAddressTable function [IP Helper], iphlp.getunicastipaddresstable, netioapi/GetUnicastIpAddressTable
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
 - GetUnicastIpAddressTable
 - netioapi/GetUnicastIpAddressTable
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
 - GetUnicastIpAddressTable
---

# GetUnicastIpAddressTable function


## -description

The 
<b>GetUnicastIpAddressTable</b> function  retrieves the unicast IP address table on the local computer.

## -parameters

### -param Family [in]

The address family to retrieve. 

Possible values for the address family are listed in the <i>Winsock2.h</i> header file. Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_INET</b> and <b>PF_INET</b>), so either constant can be used.

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and possible values for this member are defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

The values currently supported are <b>AF_INET</b>, <b>AF_INET6</b>, and <b>AF_UNSPEC</b>.

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
The address family is unspecified. When this parameter is specified,  this function returns the unicast IP address table containing both IPv4 and IPv6 entries.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 4 (IPv4) address family. When this parameter is specified,  this function returns the unicast IP address table containing only IPv4 entries. 

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 6 (IPv6) address family. When this parameter is specified,  this function returns the unicast IP address table containing only IPv6 entries.

</td>
</tr>
</table>

### -param Table [out]

A pointer to a 
<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_table">MIB_UNICASTIPADDRESS_TABLE</a> structure that contains a table of unicast IP address entries on the local computer.

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
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>Table</i> parameter or the <i>Family</i> parameter was not specified as <b>AF_INET</b>, <b>AF_INET6</b>, or <b>AF_UNSPEC</b>.

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
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Element not found. This error is returned if no  unicast IP address entries as specified in the <i>Family</i> parameter were found. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer and <b>AF_INET</b> was specified in the <b>Family</b> parameter. This error is also returned if no IPv6 stack is on the local computer and <b>AF_INET6</b> was specified in the <b>Family</b> parameter. This error is also returned on versions of Windows where this function is not supported.

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

The <b>GetUnicastIpAddressTable</b> function is defined on Windows Vista and later. 

The  
<b>GetUnicastIpAddressTable</b> function enumerates the unicast IP addresses on a local system and returns this information in an <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_table">MIB_UNICASTIPADDRESS_TABLE</a> structure. 

The unicast IP address entries are returned in a <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_table">MIB_UNICASTIPADDRESS_TABLE</a> structure in the buffer pointed to by the <i>Table</i> parameter. The <b>MIB_UNICASTIPADDRESS_TABLE</b> structure contains a unicast IP address entry count and an array of <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structures for each unicast IP address entry. When these returned structures are no longer required, free the memory by calling the <b>FreeMibTable</b>.

The <i>Family</i> parameter must be initialized to either <b>AF_INET</b>,  <b>AF_INET6</b>, or <b>AF_UNSPEC</b>. 

Note that the returned <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_table">MIB_UNICASTIPADDRESS_TABLE</a> structure pointed to by the <i>Table</i> parameter may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> array entry in the <b>Table</b> member of the <b>MIB_UNICASTIPADDRESS_TABLE</b> structure. Padding for alignment may also be present between the <b>MIB_UNICASTIPADDRESS_ROW</b> array entries. Any access to a <b>MIB_UNICASTIPADDRESS_ROW</b> array entry should assume  padding may exist. 




#### Examples

The following example retrieves a unicast IP address table and prints some values from each of the retrieved <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a> structures.


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



<b>FreeMibTable</b>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getunicastipaddressentry">GetUnicastIpAddressEntry</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-initializeunicastipaddressentry">InitializeUnicastIpAddressEntry</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row">MIB_UNICASTIPADDRESS_ROW</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_table">MIB_UNICASTIPADDRESS_TABLE</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable">NotifyStableUnicastIpAddressTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyunicastipaddresschange">NotifyUnicastIpAddressChange</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-setunicastipaddressentry">SetUnicastIpAddressEntry</a>