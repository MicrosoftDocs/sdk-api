---
UID: NF:netioapi.GetIfEntry2
title: GetIfEntry2 function (netioapi.h)
description: Retrieves information for the specified interface on the local computer.
old-location: iphlp\getifentry2.htm
tech.root: IpHlp
ms.assetid: da787dae-5e89-4bf2-a9b6-90e727995414
ms.date: 12/05/2018
ms.keywords: GetIfEntry2, GetIfEntry2 function [IP Helper], iphlp.getifentry2, netioapi/GetIfEntry2
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
 - GetIfEntry2
 - netioapi/GetIfEntry2
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
 - GetIfEntry2
---

# GetIfEntry2 function


## -description

The 
<b>GetIfEntry2</b> function  retrieves information for the specified interface on the local computer.

> [!IMPORTANT]
> For driver developers, it is recommended to use <a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2ex">GetIfEntry2Ex</a> with MibIfEntryNormalWithoutStatistics when possible, in order to avoid a deadlock when servicing NDIS OIDs.

## -parameters

### -param Row

A pointer to a 
<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a> structure that, on successful return, receives information for an interface on the local computer. On input, the <b>InterfaceLuid</b> or the <b>InterfaceIndex</b> member of the <b>MIB_IF_ROW2</b> must be set to the interface for which to retrieve information.

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
The system cannot find the file specified. This error is returned if the  network interface LUID or interface index specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a> pointed to by the <i>Row</i> parameter was not a value on the local machine.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> parameter is passed in the <i>Row</i> parameter. This error is also returned if the both the <b>InterfaceLuid</b> and <b>InterfaceIndex</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a> pointed to by the <i>Row</i> parameter  are unspecified.

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

The <b>GetIfEntry2</b> function is defined on Windows Vista and later. 

On input, at least one of the following members in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a> structure passed in the <i>Row</i> parameter must be initialized: <b>InterfaceLuid</b> or <b>InterfaceIndex</b>.

The fields are used in the order listed above. So if the <b>InterfaceLuid</b> is specified, then this member is used to determine the interface. If no value was set for the  <b>InterfaceLuid</b> member (the value of this member was set to zero), then the <b>InterfaceIndex</b> member is next used to determine the interface. 

On output, the remaining fields of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a> structure pointed to by the <i>Row</i> parameter are filled in.

Note that the <i>Netioapi.h</i> header file is automatically included in <i>Iphlpapi.h</i> header file, and should never be used directly.



#### Examples

The following example retrieves a interface entry specified on the command line and prints some values from the retrieved <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a> structure.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h>

#include <winsock2.h>
#include <ws2tcpip.h>
#include <iphlpapi.h>

#include <objbase.h>
#include <wtypes.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Iphlpapi.lib
#pragma comment(lib, "iphlpapi.lib")

// Need to link with Ole32.lib to print GUID
#pragma comment(lib, "ole32.lib")

void PrintIfEntry2(PMIB_IF_ROW2 pifRow);

int __cdecl wmain(int argc, WCHAR ** argv)
{

    // Declare and initialize variables

    ULONG retVal = 0;
    ULONG ifIndex;

    MIB_IF_ROW2 ifRow;

    // Make sure the ifRow is zeroed out
    SecureZeroMemory((PVOID) &ifRow, sizeof(MIB_IF_ROW2) );

    // Zero out the MIB_IF_ROW2 struct

    // Validate the parameters
    if (argc < 2) {
        wprintf(L"usage: %s <InterfaceIndex>\n", argv[0]);
        wprintf(L"   Gets the Interface Entry for an interface Index,\n");
        wprintf(L"Example to get the interface at interface index=6\n");
        wprintf(L"       %s 6\n", argv[0]);
        exit(1);
    }

    ifIndex = _wtoi(argv[1]);

    ifRow.InterfaceIndex = ifIndex;

    retVal = GetIfEntry2(&ifRow);

    if (retVal != NO_ERROR) {
        wprintf(L"GetIfEntry returned error: %lu\n", retVal);
        exit(1);
    }
    else
        wprintf(L"GetIfEntry2 function returned okay\n");
    
    PrintIfEntry2(&ifRow);

    exit(0);
}

// Print some parameters from the MIB_IF_ROW2 structure
void PrintIfEntry2(PMIB_IF_ROW2 pIfRow)
{

    int iRet = 0;
    WCHAR GuidString[40] = { 0 };

    unsigned int j;

    wprintf(L"\tInterfaceIndex:\t %lu\n", pIfRow->InterfaceIndex);

    iRet = StringFromGUID2(pIfRow->InterfaceGuid, (LPOLESTR) & GuidString, 39);
    // For c rather than C++ source code, the above line needs to be
    // iRet = StringFromGUID2(&pIfRow->InterfaceGuid, (LPOLESTR) &GuidString, 39); 
    if (iRet == 0)
        wprintf(L"StringFromGUID2 failed\n");
    else {
        wprintf(L"\tInterfaceGUID:   %ws\n", GuidString);
    }

    wprintf(L"\tAlias:\t\t %ws", pIfRow->Alias);
    wprintf(L"\n");
    wprintf(L"\tDescription:\t %ws", pIfRow->Description);
    wprintf(L"\n");
    wprintf(L"\tPhysical Address:\t    ");
    if (pIfRow->PhysicalAddressLength == 0)
        wprintf(L"\n");
    for (j = 0; j < (int) pIfRow->PhysicalAddressLength; j++) {
        if (j == (pIfRow->PhysicalAddressLength - 1))
            wprintf(L"%.2X\n", (int) pIfRow->PhysicalAddress[j]);
        else
            wprintf(L"%.2X-", (int) pIfRow->PhysicalAddress[j]);
    }
    wprintf(L"\tPermanent Physical Address: ");
    if (pIfRow->PhysicalAddressLength == 0)
        wprintf(L"\n");
    for (j = 0; j < (int) pIfRow->PhysicalAddressLength; j++) {
        if (j == (pIfRow->PhysicalAddressLength - 1))
            wprintf(L"%.2X\n", (int) pIfRow->PermanentPhysicalAddress[j]);
        else
            wprintf(L"%.2X-", (int) pIfRow->PermanentPhysicalAddress[j]);
    }
    wprintf(L"\tMtu:\t\t %lu\n", pIfRow->Mtu);

    wprintf(L"\tType:\t\t ");
    switch (pIfRow->Type) {
    case IF_TYPE_OTHER:
        wprintf(L"Other\n");
        break;
    case IF_TYPE_ETHERNET_CSMACD:
        wprintf(L"Ethernet\n");
        break;
    case IF_TYPE_ISO88025_TOKENRING:
        wprintf(L"Token Ring\n");
        break;
    case IF_TYPE_PPP:
        wprintf(L"PPP\n");
        break;
    case IF_TYPE_SOFTWARE_LOOPBACK:
        wprintf(L"Software Lookback\n");
        break;
    case IF_TYPE_ATM:
        wprintf(L"ATM\n");
        break;
    case IF_TYPE_IEEE80211:
        wprintf(L"IEEE 802.11 Wireless\n");
        break;
    case IF_TYPE_TUNNEL:
        wprintf(L"Tunnel type encapsulation\n");
        break;
    case IF_TYPE_IEEE1394:
        wprintf(L"IEEE 1394 Firewire\n");
        break;
    default:
        wprintf(L"Unknown type %ld\n", pIfRow->Type);
        break;
    }

    wprintf(L"\tTunnel Type:\t ");
    switch (pIfRow->TunnelType) {
    case TUNNEL_TYPE_NONE:
        wprintf(L"Not a tunnel\n");
        break;
    case TUNNEL_TYPE_OTHER:
        wprintf(L"None of the known tunnel types\n");
        break;
    case TUNNEL_TYPE_DIRECT:
        wprintf(L"Encapsulated directly within IPv4\n");
        break;
    case TUNNEL_TYPE_6TO4:
        wprintf
            (L"IPv6 packet encapsulated within IPv4 using 6to4 protocol\n");
        break;
    case TUNNEL_TYPE_ISATAP:
        wprintf
            (L"IPv6 packet encapsulated within IPv4 using ISATAP protocol\n");
        break;
    case TUNNEL_TYPE_TEREDO:
        wprintf(L"Teredo encapsulation\n");
        break;
    default:
        wprintf(L"Unknown tunnel type %ld\n", pIfRow->TunnelType);
        break;
    }

    wprintf(L"\tNDIS Media Type:\t ");
    switch (pIfRow->MediaType) {
    case NdisMedium802_3:
        wprintf(L"Ethernet (802.3)\n");
        break;
    case NdisMedium802_5:
        wprintf(L"Token Ring (802.5)\n");
        break;
    case NdisMediumFddi:
        wprintf(L"Fiber Distributed Data Interface (FDDI)\n");
        break;
    case NdisMediumWan:
        wprintf(L"Wide area network (WAN)\n");
        break;
    case NdisMediumLocalTalk:
        wprintf(L"LocalTalk\n");
        break;
    case NdisMediumDix:
        wprintf(L"Ethernet using DIX header format\n");
        break;
    case NdisMediumArcnetRaw:
        wprintf(L"ARCNET\n");
        break;
    case NdisMediumArcnet878_2:
        wprintf(L"ARCNET (878.2)\n");
        break;
    case NdisMediumAtm:
        wprintf(L"ATM\n");
        break;
    case NdisMediumWirelessWan:
        wprintf(L"Wireless WAN\n");
        break;
    case NdisMediumIrda:
        wprintf(L"Infrared (IrDA)\n");
        break;
    case NdisMediumBpc:
        wprintf(L"Broadcast PC\n");
        break;
    case NdisMediumCoWan:
        wprintf(L"Connection-oriented Wide Area Network (CoWAN)\n");
        break;
    case NdisMedium1394:
        wprintf(L"IEEE 1394 (fire wire)\n");
        break;
    case NdisMediumInfiniBand:
        wprintf(L"InfiniBand\n");
        break;
    case NdisMediumTunnel:
        wprintf(L"A Tunnel\n");
        break;
    case NdisMediumNative802_11:
        wprintf(L"Native IEEE 802.11\n");
        break;
    case NdisMediumLoopback:
        wprintf(L"NDIS loopback \n");
        break;
    default:
        wprintf(L"Unknown media type %ld\n", pIfRow->MediaType);
        break;
    }

    printf("\tAdministrative Status:\t ");
    switch (pIfRow->AdminStatus) {
    case NET_IF_ADMIN_STATUS_UP:
        wprintf(L"Interface up and enabled\n");
        break;
    case NET_IF_ADMIN_STATUS_DOWN:
        wprintf(L"Interface down\n");
        break;
    case NET_IF_ADMIN_STATUS_TESTING:
        wprintf(L"Interface in test mode\n");
        break;
    default:
        wprintf(L"Unknown status %ld\n", pIfRow->AdminStatus);
        break;
    }

    printf("\tMedia connection state:\t ");
    switch (pIfRow->MediaConnectState) {
    case MediaConnectStateUnknown:
        wprintf(L"Interface state is unknown\n");
        break;
    case MediaConnectStateConnected:
        wprintf(L"Connected\n");
        break;
    case MediaConnectStateDisconnected:
        wprintf(L"Disconnected\n");
        break;
    default:
        wprintf(L"Unknown state %ld\n", pIfRow->MediaConnectState);
        break;
    }

    wprintf(L"\tTransmit link speed:\t %I64u\n", pIfRow->TransmitLinkSpeed);
    wprintf(L"\tReceive link speed:\t %I64u\n", pIfRow->ReceiveLinkSpeed);

}

```

## -see-also

<b>GetIfEntry</b>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getiftable">GetIfTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2">GetIfTable2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2ex">GetIfTable2Ex</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow">MIB_IFROW</a>



<a href="/windows/desktop/api/ifmib/ns-ifmib-mib_iftable">MIB_IFTABLE</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_table2">MIB_IF_TABLE2</a>
