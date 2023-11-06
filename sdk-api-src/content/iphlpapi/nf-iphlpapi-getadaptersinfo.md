---
UID: NF:iphlpapi.GetAdaptersInfo
title: GetAdaptersInfo function (iphlpapi.h)
description: The GetAdaptersInfo function retrieves adapter information for the local computer.
helpviewer_keywords: ["GetAdaptersInfo","GetAdaptersInfo function [IP Helper]","_iphlp_getadaptersinfo","iphlp.getadaptersinfo","iphlpapi/GetAdaptersInfo"]
old-location: iphlp\getadaptersinfo.htm
tech.root: IpHlp
ms.assetid: 8cdecc84-6566-438b-86d0-3c55490a9a59
ms.date: 12/05/2018
ms.keywords: GetAdaptersInfo, GetAdaptersInfo function [IP Helper], _iphlp_getadaptersinfo, iphlp.getadaptersinfo, iphlpapi/GetAdaptersInfo
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
 - GetAdaptersInfo
 - iphlpapi/GetAdaptersInfo
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
 - GetAdaptersInfo
---

# GetAdaptersInfo function


## -description

The 
<b>GetAdaptersInfo</b> function retrieves adapter information for the local computer.

<b>On Windows XP and later:  </b>Use the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses">GetAdaptersAddresses</a> function instead of <b>GetAdaptersInfo</b>.

## -parameters

### -param AdapterInfo [out]

A pointer to a buffer that receives a linked list of 
<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_info">IP_ADAPTER_INFO</a> structures.

### -param SizePointer [in, out]

A pointer to a <b>ULONG</b> variable that specifies the size of the buffer pointed to by the <i>pAdapterInfo</i> parameter. If this size is insufficient to hold the adapter information, 
<b>GetAdaptersInfo</b> fills in this variable with the required size, and returns an error code of <b>ERROR_BUFFER_OVERFLOW</b>.

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
<dt><b>ERROR_BUFFER_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The buffer to receive the adapter information is too small. This value is returned if the buffer size indicated by the <i>pOutBufLen</i> parameter is too small to hold the adapter information or the <i>pAdapterInfo</i> parameter was a <b>NULL</b> pointer. When this error code is returned, the <i>pOutBufLen</i> parameter points to the required buffer size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
Invalid adapter information was retrieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid. This error is returned if the  <i>pOutBufLen</i> parameter is a <b>NULL</b> pointer, or the calling process does not have read/write access to the memory pointed to by <i>pOutBufLen</i> or the calling process does not have write access to the memory pointed to by the <i>pAdapterInfo</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_DATA</b></dt>
</dl>
</td>
<td width="60%">
No adapter information exists for the local computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersinfo">GetAdaptersInfo</a> function is not supported by the operating system running on the local computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
If the function fails, use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>GetAdaptersInfo</b> function can retrieve information only for IPv4 addresses. 

In versions prior to Windows 10, the order in which adapters appear in the list returned by this function can be controlled from the Network Connections folder: select the Advanced Settings menu item from the Advanced menu. Starting with Windows 10, the order is unspecified.

The 
<b>GetAdaptersInfo</b> and 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getinterfaceinfo">GetInterfaceInfo</a> functions do not return information about the IPv4 loopback interface. Information on the loopback interface is returned by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipaddrtable">GetIpAddrTable</a> function.

<b>On Windows XP and later:  </b>The list of adapters returned by 
<b>GetAdaptersInfo</b> includes unidirectional adapters. To generate a list of adapters that can both send and receive data, call 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo">GetUniDirectionalAdapterInfo</a>, and exclude the returned adapters from the list returned by 
<b>GetAdaptersInfo</b>.


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
                printf("Loopback\n");
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



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getinterfaceinfo">GetInterfaceInfo</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipaddrtable">GetIpAddrTable</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getnumberofinterfaces">GetNumberOfInterfaces</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getunidirectionaladapterinfo">GetUniDirectionalAdapterInfo</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_info">IP_ADAPTER_INFO</a>
