---
UID: NF:iphlpapi.SendARP
title: SendARP function (iphlpapi.h)
description: The SendARP function sends an Address Resolution Protocol (ARP) request to obtain the physical address that corresponds to the specified destination IPv4 address.
helpviewer_keywords: ["SendARP","SendARP function [IP Helper]","_iphlp_sendarp","iphlp.sendarp","iphlpapi/SendARP"]
old-location: iphlp\sendarp.htm
tech.root: IpHlp
ms.assetid: 5cbaf45a-a64e-49fd-a920-01759b5c4f81
ms.date: 12/05/2018
ms.keywords: SendARP, SendARP function [IP Helper], _iphlp_sendarp, iphlp.sendarp, iphlpapi/SendARP
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
 - SendARP
 - iphlpapi/SendARP
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
 - SendARP
---

# SendARP function


## -description

The 
<b>SendARP</b> function sends an Address Resolution Protocol (ARP) request to obtain the physical address that corresponds to the specified destination IPv4 address.

## -parameters

### -param DestIP [in]

The destination IPv4 address, in the form of an <a href="/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a> structure. The ARP request attempts to obtain the physical address that corresponds to this IPv4 address.

### -param SrcIP [in]

The source IPv4 address of the sender, in the form of an <a href="/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a> structure. This parameter is optional and is used to select the interface to send the request on for the ARP entry. The caller may specify zero corresponding to the <b>INADDR_ANY</b> IPv4 address for this parameter.

### -param pMacAddr [out]

A pointer to an array of <b>ULONG</b> variables. This array must have at least two <b>ULONG</b> elements to hold an  Ethernet or token ring physical address. The first six bytes of this array receive the physical address that corresponds to the IPv4 address specified by the <i>DestIP</i> parameter.

### -param PhyAddrLen [in, out]

On input, a pointer to a <b>ULONG</b> value that specifies the maximum buffer size, in bytes, the application has set aside to receive the physical address or MAC address. The buffer size should be at least 6 bytes for an Ethernet or token ring physical address 

The buffer to receive the physical address is pointed to by the <i>pMacAddr</i> parameter. 

On successful output, this parameter points to a value that specifies the number of bytes written to the buffer pointed to by the <i>pMacAddr</i>.

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
<dt><b>ERROR_BAD_NET_NAME</b></dt>
</dl>
</td>
<td width="60%">
The network name cannot be found. This error is returned on Windows Vista and later when an ARP reply to the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-sendarp">SendARP</a> request was not received. This error occurs  if the destination IPv4 address could not be reached because it is not on the same subnet or  the destination computer is not operating. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The file name is too long. This error is returned on Windows Vista if the  <b>ULONG</b> value pointed to by the <i>PhyAddrLen</i> parameter is less than 6, the size required to store a complete physical address. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_GEN_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
A device attached to the system is not functioning. This error is returned on Windows Server 2003 and earlier when an ARP reply to the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-sendarp">SendARP</a> request was not received. This error can occur if destination IPv4 address could not be reached because it is not on the same subnet or  the destination computer is not operating. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid. This error is returned on Windows Server 2003 and earlier if either the  <i>pMacAddr</i> or <i>PhyAddrLen</i> parameter is a <b>NULL</b> pointer. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_USER_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The supplied user buffer is not valid for the requested operation. This error is returned on Windows Server 2003 and earlier if the  <b>ULONG</b> value pointed to by the <i>PhyAddrLen</i> parameter is zero. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Element not found. This error is returned on Windows Vista if the <i>SrcIp</i> parameter does not specify a source IPv4 address on an interface on the local computer or the <b>INADDR_ANY</b> IP address (an IPv4 address of 0.0.0.0). 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-sendarp">SendARP</a> function is not supported by the operating system running on the local computer.

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

The <b>SendARP</b> function is used to request the physical hardware address (sometimes referred to as the MAC address) that corresponds to a specified destination IPv4 address. If the information requested is not in the ARP table on the local computer, then the <b>SendARP</b> function will cause an ARP request to be sent to obtain the physical address. If the function is successful, the physical address that corresponds to the specified destination IPv4 address is returned in the array pointed to by the <i>pMacAddr</i> parameter. 

The physical address of an IPv4 address is only available if the destination IPv4 address is on the local subnet (the IPv4 address can be reached directly without going through any routers). The <b>SendARP</b> function will fail if the destination IPv4 address is not on the local subnet. 

If the <b>SendARP</b> function is successful on Windows Vista and later, the ARP table on the local computer is updated with the results.  If the <b>SendARP</b> function is successful on Windows Server 2003 and earlier, the ARP table on the local computer is not affected. 

The <b>SendARP</b> function on Windows Vista and later returns different error return values  than the  <b>SendARP</b> function on    Windows Server 2003 and earlier. 

 On Windows Vista and later, a <b>NULL</b> pointer passed as the <i>pMacAddr</i> or <i>PhyAddrLen</i> parameter to the <b>SendARP</b> function causes an access violation and the application is terminated. If an error occurs on Windows Vista and later and <b>ERROR_BAD_NET_NAME</b>,  <b>ERROR_BUFFER_OVERFLOW</b>, or <b>ERROR_NOT_FOUND</b> is returned, the <b>ULONG</b> value pointed to by the <i>PhyAddrLen</i> parameter is set to zero. If the <b>ULONG</b> value pointed to by the <i>PhyAddrLen</i> parameter is less than 6 on  Windows Vista and later, <b>SendARP</b> function returns  <b>ERROR_BUFFER_OVERFLOW</b> indicating the buffer to receive the physical address is too small. If the <i>SrcIp</i> parameter specifies an IPv4 address that is not an interface on the local computer, the <b>SendARP</b> function on    Windows Vista and later  returns <b>ERROR_NOT_FOUND</b>. 

 On Windows Server 2003 and earlier, a <b>NULL</b> pointer passed as the <i>pMacAddr</i> or <i>PhyAddrLen</i> parameter to the <b>SendARP</b> function returns <b>ERROR_INVALID_PARAMETER</b>. If an error occurs on Windows Server 2003 and earlier and <b>ERROR_GEN_FAILURE</b> or   <b>ERROR_INVALID_USER_BUFFER</b> is returned, the <b>ULONG</b> value pointed to by the <i>PhyAddrLen</i> parameter is set to zero. If the <b>ULONG</b> value pointed to by the <i>PhyAddrLen</i> parameter is less than 6 on  Windows Server 2003 and earlier, the <b>SendARP</b> function does not return an error but only returns part of the hardware address in the array pointed to by the <i>pMacAddr</i> parameter. So if the value pointed to by the <i>PhyAddrLen</i> parameter is 4, then only the first 4 bytes of the hardware address are returned in the array pointed to by the <i>pMacAddr</i> parameter. If the <i>SrcIp</i> parameter specifies an IPv4 address that is not an interface on the local computer, the <b>SendARP</b> function on    Windows Server 2003 and  earlier ignores the <i>SrcIp</i> parameter and uses an IPv4 address on the local computer for the source IPv4 address. 

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipnettable">GetIpNetTable</a> function retrieves the ARP table on the local computer that maps IPv4 addresses to physical addresses.

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createipnetentry">CreateIpNetEntry</a> function creates an ARP entry in the ARP table on the local computer.

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipnetentry">DeleteIpNetEntry</a> function deletes an ARP entry from the ARP table on the local computer.

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipnetentry">SetIpNetEntry</a> function modifies an existing ARP entry in the ARP table on the local computer.

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-flushipnettable">FlushIpNetTable</a> function deletes all ARP entries for the specified interface from the ARP table on the local computer. 



On Windows Vista and later, the <a href="/windows/desktop/api/netioapi/nf-netioapi-resolveipnetentry2">ResolveIpNetEntry2</a> function can used to replace the <b>SendARP</b> function. An ARP request is sent if the <b>Address</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipnet_row2">MIB_IPNET_ROW2</a> structure passed to the <b>ResolveIpNetEntry2</b> function is an IPv4 address.  

On Windows Vista, a new group of functions can be used to access, modify, and delete the ARP table entries when the <b>Address</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipnet_row2">MIB_IPNET_ROW2</a> structure passed to these functions is an IPv4 address.  The new functions include the following: <a href="/windows/desktop/api/netioapi/nf-netioapi-getipnettable2">GetIpNetTable2</a>, <a href="/windows/desktop/api/netioapi/nf-netioapi-createipnetentry2">CreateIpNetEntry2</a>, <a href="/windows/desktop/api/netioapi/nf-netioapi-deleteipnetentry2">DeleteIpNetEntry2</a>,  <a href="/windows/desktop/api/netioapi/nf-netioapi-flushipnettable2">FlushIpNetTable2</a>, and <a href="/windows/desktop/api/netioapi/nf-netioapi-setipnetentry2">SetIpNetEntry2</a>.

For information about the <b>IPAddr</b> data type, see 
<a href="/windows/desktop/WinProg/windows-data-types">Windows Data Types</a>. To convert an IP address between dotted decimal notation and <b>IPAddr</b> format, use the 
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_addr">inet_addr</a> and 
<a href="/windows/desktop/api/wsipv6ok/nf-wsipv6ok-inet_ntoa">inet_ntoa</a> functions.


#### Examples

The following code demonstrates how to obtain the hardware or media access control (MAC) address associated with a specified IPv4 address.


```cpp
#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <winsock2.h>
#include <iphlpapi.h>
#include <stdio.h>
#include <stdlib.h>

#pragma comment(lib, "iphlpapi.lib")
#pragma comment(lib, "ws2_32.lib")

void usage(char *pname)
{
    printf("Usage: %s [options] ip-address\n", pname);
    printf("\t -h \t\thelp\n");
    printf("\t -l length \tMAC physical address length to set\n");
    printf("\t -s src-ip \tsource IP address\n");
    exit(1);
}

int __cdecl main(int argc, char **argv)
{
    DWORD dwRetVal;
    IPAddr DestIp = 0;
    IPAddr SrcIp = 0;       /* default for src ip */
    ULONG MacAddr[2];       /* for 6-byte hardware addresses */
    ULONG PhysAddrLen = 6;  /* default to length of six bytes */

    char *DestIpString = NULL;
    char *SrcIpString = NULL;

    BYTE *bPhysAddr;
    unsigned int i;

    if (argc > 1) {
        for (i = 1; i < (unsigned int) argc; i++) {
            if ((argv[i][0] == '-') || (argv[i][0] == '/')) {
                switch (tolower(argv[i][1])) {
                case 'l':
                    PhysAddrLen = (ULONG) atol(argv[++i]);
                    break;
                case 's':
                    SrcIpString = argv[++i];
                    SrcIp = inet_addr(SrcIpString);
                    break;
                case 'h':
                default:
                    usage(argv[0]);
                    break;
                }               /* end switch */
            } else
                DestIpString = argv[i];
        }                       /* end for */
    } else
        usage(argv[0]);

    if (DestIpString == NULL || DestIpString[0] == '\0')
        usage(argv[0]);

    DestIp = inet_addr(DestIpString);

    memset(&MacAddr, 0xff, sizeof (MacAddr));

    printf("Sending ARP request for IP address: %s\n", DestIpString);

    dwRetVal = SendARP(DestIp, SrcIp, &MacAddr, &PhysAddrLen);

    if (dwRetVal == NO_ERROR) {
        bPhysAddr = (BYTE *) & MacAddr;
        if (PhysAddrLen) {
            for (i = 0; i < (int) PhysAddrLen; i++) {
                if (i == (PhysAddrLen - 1))
                    printf("%.2X\n", (int) bPhysAddr[i]);
                else
                    printf("%.2X-", (int) bPhysAddr[i]);
            }
        } else
            printf
                ("Warning: SendArp completed successfully, but returned length=0\n");

    } else {
        printf("Error: SendArp failed with error: %d", dwRetVal);
        switch (dwRetVal) {
        case ERROR_GEN_FAILURE:
            printf(" (ERROR_GEN_FAILURE)\n");
            break;
        case ERROR_INVALID_PARAMETER:
            printf(" (ERROR_INVALID_PARAMETER)\n");
            break;
        case ERROR_INVALID_USER_BUFFER:
            printf(" (ERROR_INVALID_USER_BUFFER)\n");
            break;
        case ERROR_BAD_NET_NAME:
            printf(" (ERROR_GEN_FAILURE)\n");
            break;
        case ERROR_BUFFER_OVERFLOW:
            printf(" (ERROR_BUFFER_OVERFLOW)\n");
            break;
        case ERROR_NOT_FOUND:
            printf(" (ERROR_NOT_FOUND)\n");
            break;
        default:
            printf("\n");
            break;
        }
    }

    return 0;
}


```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createipnetentry">CreateIpNetEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-createipnetentry2">CreateIpNetEntry2</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createproxyarpentry">CreateProxyArpEntry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipnetentry">DeleteIpNetEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-deleteipnetentry2">DeleteIpNetEntry2</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteproxyarpentry">DeleteProxyArpEntry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-flushipnettable">FlushIpNetTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-flushipnettable2">FlushIpNetTable2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipnetentry2">GetIpNetEntry2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipnettable2">GetIpNetTable2</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper
		  Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper
		  Start Page</a>



<a href="/windows/desktop/api/inaddr/ns-inaddr-in_addr">IPAddr</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-resolveipnetentry2">ResolveIpNetEntry2</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipnetentry">SetIpNetEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-setipnetentry2">SetIpNetEntry2</a>