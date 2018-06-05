---
UID: NS:netioapi._MIB_UNICASTIPADDRESS_TABLE
title: "_MIB_UNICASTIPADDRESS_TABLE"
author: windows-sdk-content
description: Contains a table of unicast IP address entries.
old-location: mib\mib_unicastipaddress_table.htm
old-project: MIB
ms.assetid: b064494c-d0d5-4570-b255-4cc95412fd3a
ms.author: windowssdkdev
ms.date: 05/14/2018
ms.keywords: "*PMIB_UNICASTIPADDRESS_TABLE, MIB_UNICASTIPADDRESS_TABLE, MIB_UNICASTIPADDRESS_TABLE structure [MIB], PMIB_UNICASTIPADDRESS_TABLE, PMIB_UNICASTIPADDRESS_TABLE structure pointer [MIB], _MIB_UNICASTIPADDRESS_TABL, _MIB_UNICASTIPADDRESS_TABLE, mib.mib_unicastipaddress_table, netioapi/MIB_UNICASTIPADDRESS_TABLE, netioapi/PMIB_UNICASTIPADDRESS_TABLE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: MIB_UNICASTIPADDRESS_TABLE, *PMIB_UNICASTIPADDRESS_TABLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Netioapi.h
api_name:
-	MIB_UNICASTIPADDRESS_TABLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _MIB_UNICASTIPADDRESS_TABLE structure


## -description


The 
<b>MIB_UNICASTIPADDRESS_TABLE</b> structure contains a table of unicast IP address entries.


## -struct-fields




### -field NumEntries

A value that specifies the number of unicast IP address entries in the array.


### -field Table

An array of 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff559308">MIB_UNICASTIPADDRESS_ROW</a> structures containing unicast IP address entries.


## -remarks



The <b>MIB_UNICASTIPADDRESS_TABLE</b> structure is defined on Windows Vista and later. 

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff552594">GetUnicastIpAddressTable</a> function enumerates the unicast IP addresses on a local system and returns this information in an <b>MIB_UNICASTIPADDRESS_TABLE</b> structure. 



The <b>MIB_UNICASTIPADDRESS_TABLE</b> structure may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="https://msdn.microsoft.com/library/windows/hardware/ff559308">MIB_UNICASTIPADDRESS_ROW</a> array entry in the <b>Table</b> member. Padding for alignment may also be present between the <b>MIB_UNICASTIPADDRESS_ROW</b> array entries in the <b>Table</b> member. Any access to a <b>MIB_UNICASTIPADDRESS_ROW</b> array entry should assume  padding may exist. 




#### Examples

The following example retrieves a unicast IP address table and prints some values from each of the retrieved <a href="https://msdn.microsoft.com/library/windows/hardware/ff559308">MIB_UNICASTIPADDRESS_ROW</a> structures.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include &lt;Windows.h.&gt;
#include &lt;winsock2.h&gt;
#include &lt;ws2tcpip.h&gt;
#include &lt;ws2ipdef.h&gt;
#include &lt;iphlpapi.h&gt;
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

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

    Result = GetUnicastIpAddressTable(AF_UNSPEC, &amp;pipTable);
    if (Result != NO_ERROR) {
        wprintf(L"GetUnicastIpAddressTable returned error: %ld\n", Result);
        exit(1);
    }
    // Print some variables from the rows in the table
    wprintf(L"Number of table entries: %d\n\n", pipTable-&gt;NumEntries);

    for (i = 0; i &lt; pipTable-&gt;NumEntries; i++) {
        wprintf(L"AddressFamily[%d]:\t\t ", i);

        switch (pipTable-&gt;Table[i].Address.si_family) {
        case AF_INET:
            wprintf(L"IPv4\n");
            if (InetNtopW
                (AF_INET, &amp;pipTable-&gt;Table[i].Address.Ipv4.sin_addr, Ipv4String,
                 16) != NULL)
                wprintf(L"IPv4 Address:\t\t\t %ws\n", Ipv4String);
            break;
        case AF_INET6:
            wprintf(L"IPv6\n");
            if (InetNtopW
                (AF_INET6, &amp;pipTable-&gt;Table[i].Address.Ipv6.sin6_addr,
                 Ipv6String, 46) != NULL)
                wprintf(L"IPv6 Address:\t\t\t %ws\n", Ipv6String);
            break;
        default:
            wprintf(L"Other: %d\n", pipTable-&gt;Table[i].Address.si_family);
            break;
        }

        wprintf(L"Interface LUID NetLuidIndex[%d]:  %lu\n",
               i, pipTable-&gt;Table[i].InterfaceLuid.Info.NetLuidIndex);
        wprintf(L"Interface LUID IfType[%d]:\t ", i);
        switch (pipTable-&gt;Table[i].InterfaceLuid.Info.IfType) {
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
                   pipTable-&gt;Table[i].InterfaceLuid.Info.IfType);
            break;
        }

        wprintf(L"Interface Index[%d]:\t\t %lu\n",
               i, pipTable-&gt;Table[i].InterfaceIndex);

        wprintf(L"Prefix Origin[%d]:\t\t ", i);
        switch (pipTable-&gt;Table[i].PrefixOrigin) {
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
            wprintf(L"Unknown: %d\n", pipTable-&gt;Table[i].PrefixOrigin);
            break;
        }

        wprintf(L"Suffix Origin[%d]:\t\t ", i);
        switch (pipTable-&gt;Table[i].SuffixOrigin) {
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
            wprintf(L"Unknown: %d\n", pipTable-&gt;Table[i].SuffixOrigin);
            break;
        }

        wprintf(L"Valid Lifetime[%d]:\t\t 0x%x (%u)\n", i,
               pipTable-&gt;Table[i].ValidLifetime,
               pipTable-&gt;Table[i].ValidLifetime);

        wprintf(L"Preferred Lifetime[%d]:\t\t 0x%x (%u)\n", i,
               pipTable-&gt;Table[i].PreferredLifetime,
               pipTable-&gt;Table[i].PreferredLifetime);

        wprintf(L"OnLink PrefixLength[%d]:\t\t %lu\n", i,
               pipTable-&gt;Table[i].OnLinkPrefixLength);

        wprintf(L"Skip As Source[%d]:\t\t ", i);
        if (pipTable-&gt;Table[i].SkipAsSource)
            wprintf(L"Yes\n");
        else
            wprintf(L"No\n");

        wprintf(L"Dad State[%d]:\t\t\t ", i);
        switch (pipTable-&gt;Table[i].DadState) {
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
            wprintf(L"Unknown: %d\n", pipTable-&gt;Table[i].DadState);
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

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552594">GetUnicastIpAddressTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff559308">MIB_UNICASTIPADDRESS_ROW</a>
 

 

