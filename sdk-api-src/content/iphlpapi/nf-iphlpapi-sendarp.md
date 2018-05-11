---
UID: NF:iphlpapi.SendARP
title: SendARP function
author: windows-driver-content
description: The SendARP function sends an Address Resolution Protocol (ARP) request to obtain the physical address that corresponds to the specified destination IPv4 address.
old-location: iphlp\sendarp.htm
old-project: IpHlp
ms.assetid: 5cbaf45a-a64e-49fd-a920-01759b5c4f81
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: SendARP, SendARP function [IP Helper], _iphlp_sendarp, iphlp.sendarp, iphlpapi/SendARP
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
-	SendARP
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# SendARP function


## -description



			The 
<b>SendARP</b> function sends an Address Resolution Protocol (ARP) request to obtain the physical address that corresponds to the specified destination IPv4 address.


## -parameters




### -param DestIP [in]

The destination IPv4 address, in the form of an <a href="https://msdn.microsoft.com/00d4823d-114d-4cc7-afdf-54c7fed3fe45">IPAddr</a> structure. The ARP request attempts to obtain the physical address that corresponds to this IPv4 address.


### -param SrcIP [in]

The source IPv4 address of the sender, in the form of an <a href="https://msdn.microsoft.com/00d4823d-114d-4cc7-afdf-54c7fed3fe45">IPAddr</a> structure. This parameter is optional and is used to select the interface to send the request on for the ARP entry. The caller may specify zero corresponding to the <b>INADDR_ANY</b> IPv4 address for this parameter.


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
The network name cannot be found. This error is returned on Windows Vista and later when an ARP reply to the <a href="https://msdn.microsoft.com/5cbaf45a-a64e-49fd-a920-01759b5c4f81">SendARP</a> request was not received. This error occurs  if the destination IPv4 address could not be reached because it is not on the same subnet or  the destination computer is not operating. 

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
A device attached to the system is not functioning. This error is returned on Windows Server 2003 and earlier when an ARP reply to the <a href="https://msdn.microsoft.com/5cbaf45a-a64e-49fd-a920-01759b5c4f81">SendARP</a> request was not received. This error can occur if destination IPv4 address could not be reached because it is not on the same subnet or  the destination computer is not operating. 

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
Element not found. This error is returned on Windows Vista if the  the <i>SrcIp</i> parameter does not specify a source IPv4 address on an interface on the local computer or the <b>INADDR_ANY</b> IP address (an IPv4 address of 0.0.0.0). 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">

								The <a href="https://msdn.microsoft.com/5cbaf45a-a64e-49fd-a920-01759b5c4f81">SendARP</a> function is not supported by the operating system running on the local computer.

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



The <b>SendARP</b> function is used to request the physical hardware address (sometimes referred to as the MAC address) that corresponds to a specified destination IPv4 address. If the information requested is not in the ARP table on the local computer, then the <b>SendARP</b> function will cause an ARP request to be sent to obtain the physical address. If the function is successful, the physical address that corresponds to the specified destination IPv4 address is returned in the array pointed to by the <i>pMacAddr</i> parameter. 

The physical address of an IPv4 address is only available if the destination IPv4 address is on the local subnet (the IPv4 address can be reached directly without going through any routers). The <b>SendARP</b> function will fail if the destination IPv4 address is not on the local subnet. 

If the <b>SendARP</b> function is successful on Windows Vista and later, the ARP table on the local computer is updated with the results.  If the <b>SendARP</b> function is successful on Windows Server 2003 and earlier, the ARP table on the local computer is not affected. 

The <b>SendARP</b> function on Windows Vista and later returns different error return values  than the  <b>SendARP</b> function on    Windows Server 2003 and earlier. 

 On Windows Vista and later, a <b>NULL</b> pointer passed as the <i>pMacAddr</i> or <i>PhyAddrLen</i> parameter to the <b>SendARP</b> function causes an access violation and the application is terminated. If an error occurs on Windows Vista and later and <b>ERROR_BAD_NET_NAME</b>,  <b>ERROR_BUFFER_OVERFLOW</b>, or <b>ERROR_NOT_FOUND</b> is returned, the <b>ULONG</b> value pointed to by the <i>PhyAddrLen</i> parameter is set to zero. If the <b>ULONG</b> value pointed to by the <i>PhyAddrLen</i> parameter is less than 6 on  Windows Vista and later, <b>SendARP</b> function returns  <b>ERROR_BUFFER_OVERFLOW</b> indicating the buffer to receive the physical address is too small. If the <i>SrcIp</i> parameter specifies an IPv4 address that is not an interface on the local computer, the <b>SendARP</b> function on    Windows Vista and later  returns <b>ERROR_NOT_FOUND</b>. 

 On Windows Server 2003 and earlier, a <b>NULL</b> pointer passed as the <i>pMacAddr</i> or <i>PhyAddrLen</i> parameter to the <b>SendARP</b> function returns <b>ERROR_INVALID_PARAMETER</b>. If an error occurs on Windows Server 2003 and earlier and <b>ERROR_GEN_FAILURE</b> or   <b>ERROR_INVALID_USER_BUFFER</b> is returned, the <b>ULONG</b> value pointed to by the <i>PhyAddrLen</i> parameter is set to zero. If the <b>ULONG</b> value pointed to by the <i>PhyAddrLen</i> parameter is less than 6 on  Windows Server 2003 and earlier, the <b>SendARP</b> function does not return an error but only returns part of the hardware address in the array pointed to by the <i>pMacAddr</i> parameter. So if the value pointed to by the <i>PhyAddrLen</i> parameter is 4, then only the first 4 bytes of the hardware address are returned in the array pointed to by the <i>pMacAddr</i> parameter. If the <i>SrcIp</i> parameter specifies an IPv4 address that is not an interface on the local computer, the <b>SendARP</b> function on    Windows Server 2003 and  earlier ignores the <i>SrcIp</i> parameter and uses an IPv4 address on the local computer for the source IPv4 address. 

The <a href="https://msdn.microsoft.com/01bcf86e-5fcc-4ce9-bb89-02d393e75d1d">GetIpNetTable</a> function retrieves the ARP table on the local computer that maps IPv4 addresses to physical addresses.

The <a href="https://msdn.microsoft.com/607f9aad-2046-4ab2-9a62-4092f87ffa66">CreateIpNetEntry</a> function creates an ARP entry in the ARP table on the local computer.

The <a href="https://msdn.microsoft.com/0d338676-b66f-410c-8022-5576096954b4">DeleteIpNetEntry</a> function deletes an ARP entry from the ARP table on the local computer.

The <a href="https://msdn.microsoft.com/d985b749-5aa3-4b4a-ba8f-bc8edcf1b1f3">SetIpNetEntry</a> function modifies an existing ARP entry in the ARP table on the local computer.

The <a href="https://msdn.microsoft.com/cf4dea10-552d-4730-a452-9302ef3761ff">FlushIpNetTable</a> function deletes all ARP entries for the specified interface from the ARP table on the local computer. 



On Windows Vista and later, the <a href="https://msdn.microsoft.com/library/windows/hardware/ff570686">ResolveIpNetEntry2</a> function can used to replace the <b>SendARP</b> function. An ARP request is sent if the <b>Address</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559263">MIB_IPNET_ROW2</a> structure passed to the <b>ResolveIpNetEntry2</b> function is an IPv4 address.  

On Windows Vista, a new group of functions can be used to access, modify, and delete the ARP table entries when the <b>Address</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff559263">MIB_IPNET_ROW2</a> structure passed to these functions is an IPv4 address.  The new functions include the following: <a href="https://msdn.microsoft.com/library/windows/hardware/ff552551">GetIpNetTable2</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff546217">CreateIpNetEntry2</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/ff546368">DeleteIpNetEntry2</a>,  <a href="https://msdn.microsoft.com/library/windows/hardware/ff550029">FlushIpNetTable2</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/ff570775">SetIpNetEntry2</a>.

For information about the <b>IPAddr</b> data type, see 
<a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">Windows Data Types</a>. To convert an IP address between dotted decimal notation and <b>IPAddr</b> format, use the 
<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a> and 
<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a> functions.


#### Examples

The following code demonstrates how to obtain the hardware or media access control (MAC) address associated with a specified IPv4 address.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include &lt;winsock2.h&gt;
#include &lt;iphlpapi.h&gt;
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

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

    if (argc &gt; 1) {
        for (i = 1; i &lt; (unsigned int) argc; i++) {
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

    memset(&amp;MacAddr, 0xff, sizeof (MacAddr));

    printf("Sending ARP request for IP address: %s\n", DestIpString);

    dwRetVal = SendARP(DestIp, SrcIp, &amp;MacAddr, &amp;PhysAddrLen);

    if (dwRetVal == NO_ERROR) {
        bPhysAddr = (BYTE *) &amp; MacAddr;
        if (PhysAddrLen) {
            for (i = 0; i &lt; (int) PhysAddrLen; i++) {
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

</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/607f9aad-2046-4ab2-9a62-4092f87ffa66">CreateIpNetEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546217">CreateIpNetEntry2</a>



<a href="https://msdn.microsoft.com/a0e90c0a-9403-40cb-906e-6e1e2f8e73c4">CreateProxyArpEntry</a>



<a href="https://msdn.microsoft.com/0d338676-b66f-410c-8022-5576096954b4">DeleteIpNetEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546368">DeleteIpNetEntry2</a>



<a href="https://msdn.microsoft.com/26e08e4d-ac69-49f8-8a1a-1ba1a04d085c">DeleteProxyArpEntry</a>



<a href="https://msdn.microsoft.com/cf4dea10-552d-4730-a452-9302ef3761ff">FlushIpNetTable</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550029">FlushIpNetTable2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552546">GetIpNetEntry2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552551">GetIpNetTable2</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper
		  Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper
		  Start Page</a>



<a href="https://msdn.microsoft.com/00d4823d-114d-4cc7-afdf-54c7fed3fe45">IPAddr</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570686">ResolveIpNetEntry2</a>



<a href="https://msdn.microsoft.com/d985b749-5aa3-4b4a-ba8f-bc8edcf1b1f3">SetIpNetEntry</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff570775">SetIpNetEntry2</a>
 

 

