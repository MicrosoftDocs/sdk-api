---
UID: NF:iphlpapi.GetAdaptersInfo
title: GetAdaptersInfo function
author: windows-driver-content
description: The GetAdaptersInfo function retrieves adapter information for the local computer.
old-location: iphlp\getadaptersinfo.htm
old-project: IpHlp
ms.assetid: 8cdecc84-6566-438b-86d0-3c55490a9a59
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetAdaptersInfo, GetAdaptersInfo function [IP Helper], _iphlp_getadaptersinfo, iphlp.getadaptersinfo, iphlpapi/GetAdaptersInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: NET_ADDRESS_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iphlpapi.dll
api_name:
-	GetAdaptersInfo
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetAdaptersInfo function


## -description


The 
<b>GetAdaptersInfo</b> function retrieves adapter information for the local computer.

<b>On Windows XP and later:  </b>Use the  
<a href="https://msdn.microsoft.com/7b34138f-7263-4b73-95df-9e854fd81135">GetAdaptersAddresses</a> function instead of <b>GetAdaptersInfo</b>.


## -parameters




### -param AdapterInfo

TBD


### -param SizePointer

TBD




#### - pAdapterInfo [out]

A pointer to a buffer that receives a linked list of 
<a href="https://msdn.microsoft.com/f8035801-ca0c-4d86-bfc5-8e2d746af1b4">IP_ADAPTER_INFO</a> structures.


#### - pOutBufLen [in, out]

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

								The <a href="https://msdn.microsoft.com/8cdecc84-6566-438b-86d0-3c55490a9a59">GetAdaptersInfo</a> function is not supported by the operating system running on the local computer.

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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The  
<b>GetAdaptersInfo</b> function can retrieve information only for IPv4 addresses. 

In versions prior to Windows 10, the order in which adapters appear in the list returned by this function can be controlled from the Network Connections folder: select the Advanced Settings menu item from the Advanced menu. Starting with Windows 10, the order is unspecified.

The 
<b>GetAdaptersInfo</b> and 
<a href="https://msdn.microsoft.com/efc0d175-2c6d-4608-b385-1623a9e0375c">GetInterfaceInfo</a> functions do not return information about the IPv4 loopback interface. Information on the loopback interface is returned by the <a href="https://msdn.microsoft.com/03bf5645-8237-4c78-a921-47315cab1c44">GetIpAddrTable</a> function.

<b>On Windows XP and later:  </b>The list of adapters returned by 
<b>GetAdaptersInfo</b> includes unidirectional adapters. To generate a list of adapters that can both send and receive data, call 
<a href="https://msdn.microsoft.com/32aa3a8e-ae74-4da9-bc8d-b28e270d9702">GetUniDirectionalAdapterInfo</a>, and exclude the returned adapters from the list returned by 
<b>GetAdaptersInfo</b>.


#### Examples

This example retrieves the adapter information and prints various properties of each adapter.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;winsock2.h&gt;
#include &lt;iphlpapi.h&gt;
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;
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
    if (GetAdaptersInfo(pAdapterInfo, &amp;ulOutBufLen) == ERROR_BUFFER_OVERFLOW) {
        FREE(pAdapterInfo);
        pAdapterInfo = (IP_ADAPTER_INFO *) MALLOC(ulOutBufLen);
        if (pAdapterInfo == NULL) {
            printf("Error allocating memory needed to call GetAdaptersinfo\n");
            return 1;
        }
    }

    if ((dwRetVal = GetAdaptersInfo(pAdapterInfo, &amp;ulOutBufLen)) == NO_ERROR) {
        pAdapter = pAdapterInfo;
        while (pAdapter) {
            printf("\tComboIndex: \t%d\n", pAdapter-&gt;ComboIndex);
            printf("\tAdapter Name: \t%s\n", pAdapter-&gt;AdapterName);
            printf("\tAdapter Desc: \t%s\n", pAdapter-&gt;Description);
            printf("\tAdapter Addr: \t");
            for (i = 0; i &lt; pAdapter-&gt;AddressLength; i++) {
                if (i == (pAdapter-&gt;AddressLength - 1))
                    printf("%.2X\n", (int) pAdapter-&gt;Address[i]);
                else
                    printf("%.2X-", (int) pAdapter-&gt;Address[i]);
            }
            printf("\tIndex: \t%d\n", pAdapter-&gt;Index);
            printf("\tType: \t");
            switch (pAdapter-&gt;Type) {
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
                printf("Unknown type %ld\n", pAdapter-&gt;Type);
                break;
            }

            printf("\tIP Address: \t%s\n",
                   pAdapter-&gt;IpAddressList.IpAddress.String);
            printf("\tIP Mask: \t%s\n", pAdapter-&gt;IpAddressList.IpMask.String);

            printf("\tGateway: \t%s\n", pAdapter-&gt;GatewayList.IpAddress.String);
            printf("\t***\n");

            if (pAdapter-&gt;DhcpEnabled) {
                printf("\tDHCP Enabled: Yes\n");
                printf("\t  DHCP Server: \t%s\n",
                       pAdapter-&gt;DhcpServer.IpAddress.String);

                printf("\t  Lease Obtained: ");
                /* Display local time */
                error = _localtime32_s(&amp;newtime, (__time32_t*) &amp;pAdapter-&gt;LeaseObtained);
                if (error)
                    printf("Invalid Argument to _localtime32_s\n");
                else {
                    // Convert to an ASCII representation 
                    error = asctime_s(buffer, 32, &amp;newtime);
                    if (error)
                        printf("Invalid Argument to asctime_s\n");
                    else
                        /* asctime_s returns the string terminated by \n\0 */
                        printf("%s", buffer);
                }

                printf("\t  Lease Expires:  ");
                error = _localtime32_s(&amp;newtime, (__time32_t*) &amp;pAdapter-&gt;LeaseExpires);
                if (error)
                    printf("Invalid Argument to _localtime32_s\n");
                else {
                    // Convert to an ASCII representation 
                    error = asctime_s(buffer, 32, &amp;newtime);
                    if (error)
                        printf("Invalid Argument to asctime_s\n");
                    else
                        /* asctime_s returns the string terminated by \n\0 */
                        printf("%s", buffer);
                }
            } else
                printf("\tDHCP Enabled: No\n");

            if (pAdapter-&gt;HaveWins) {
                printf("\tHave Wins: Yes\n");
                printf("\t  Primary Wins Server:    %s\n",
                       pAdapter-&gt;PrimaryWinsServer.IpAddress.String);
                printf("\t  Secondary Wins Server:  %s\n",
                       pAdapter-&gt;SecondaryWinsServer.IpAddress.String);
            } else
                printf("\tHave Wins: No\n");
            pAdapter = pAdapter-&gt;Next;
            printf("\n");
        }
    } else {
        printf("GetAdaptersInfo failed with error: %d\n", dwRetVal);

    }
    if (pAdapterInfo)
        FREE(pAdapterInfo);

    return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7b34138f-7263-4b73-95df-9e854fd81135">GetAdaptersAddresses</a>



<a href="https://msdn.microsoft.com/efc0d175-2c6d-4608-b385-1623a9e0375c">GetInterfaceInfo</a>



<a href="https://msdn.microsoft.com/03bf5645-8237-4c78-a921-47315cab1c44">GetIpAddrTable</a>



<a href="https://msdn.microsoft.com/655d63eb-455a-4a5e-97e2-7b7588eee4d9">GetNumberOfInterfaces</a>



<a href="https://msdn.microsoft.com/32aa3a8e-ae74-4da9-bc8d-b28e270d9702">GetUniDirectionalAdapterInfo</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/f8035801-ca0c-4d86-bfc5-8e2d746af1b4">IP_ADAPTER_INFO</a>
 

 

