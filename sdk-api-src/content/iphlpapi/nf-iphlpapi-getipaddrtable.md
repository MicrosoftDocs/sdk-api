---
UID: NF:iphlpapi.GetIpAddrTable
title: GetIpAddrTable function (iphlpapi.h)
author: windows-sdk-content
description: The GetIpAddrTable function retrieves the interface&#8211;to&#8211;IPv4 address mapping table.
old-location: iphlp\getipaddrtable.htm
tech.root: IpHlp
ms.assetid: 03bf5645-8237-4c78-a921-47315cab1c44
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetIpAddrTable, GetIpAddrTable function [IP Helper], _iphlp_getipaddrtable, iphlp.getipaddrtable, iphlpapi/GetIpAddrTable
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetIpAddrTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetIpAddrTable function


## -description


The 
<b>GetIpAddrTable</b> function retrieves the interface–to–IPv4 address mapping table.


## -parameters




### -param pIpAddrTable [out]

A pointer to a buffer that receives the interface–to–IPv4 address mapping table as a 
<a href="https://msdn.microsoft.com/12a929e5-813d-4dae-9ea0-5a3c0a88cf05">MIB_IPADDRTABLE</a> structure.


### -param pdwSize [in, out]

On input, specifies the size in bytes  of the buffer pointed to by the <i>pIpAddrTable</i> parameter. 




On output, if the buffer is not large enough to hold the returned mapping table, the function sets this parameter equal to the required buffer size in bytes.


### -param bOrder [in]

A Boolean value that specifies whether the returned mapping table should be sorted in ascending order by IPv4 address. If this parameter is <b>TRUE</b>, the table is sorted.


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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>pIpAddrTable</i> parameter is not large enough. The required size is returned in the <b>DWORD</b> variable pointed to by the <i>pdwSize</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwSize</i> parameter is <b>NULL</b>, or 
<a href="https://msdn.microsoft.com/03bf5645-8237-4c78-a921-47315cab1c44">GetIpAddrTable</a> is unable to write to the memory pointed to by the <i>pdwSize</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This function is not supported on the operating system in use on the local system.

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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>GetIpAddrTable</b> function retrieves the interface–to–IPv4 address mapping table on a local computer and returns this information in an <a href="https://msdn.microsoft.com/12a929e5-813d-4dae-9ea0-5a3c0a88cf05">MIB_IPADDRTABLE</a> structure.

The IPv4 addresses returned by the <b>GetIpAddrTable</b> function are affected by the status of the network interfaces on a local computer. Manually resetting a network interface card (NIC) and certain PnP events may result in an IP address being removed or changed. 

On Windows Server 2003 and Windows XP, the IPv4 addresses returned by the <b>GetIpAddrTable</b> function are also affected if the media sensing capability of the TCP/IP stack on a local computer has been disabled by calling the <a href="https://msdn.microsoft.com/ec845db8-d544-4291-8221-0fde82c2de27">DisableMediaSense</a> function. When media sensing has been disabled, the <b>GetIpAddrTable</b> function may return IPv4 addresses associated with disconnected interfaces. These Ipv4 addresses for disconnected interfaces are not valid for use. 

On Windows Server 2008 and Windows Vista, the IPv4 addresses returned by the <b>GetIpAddrTable</b> function are not affected by the media sensing capability of the TCP/IP stack on a local computer. The <b>GetIpAddrTable</b> function returns only valid IPv4 addresses. 

The <a href="https://msdn.microsoft.com/7b34138f-7263-4b73-95df-9e854fd81135">GetAdaptersAddresses</a> function available on Windows XP can be used to retrieve both IPv6 and IPv4 addresses and interface information. 

The <a href="https://msdn.microsoft.com/12a929e5-813d-4dae-9ea0-5a3c0a88cf05">MIB_IPADDRTABLE</a> structure returned by the <b>GetIpAddrTable</b> function may contain padding for alignment between the <b>dwNumEntries</b> member and the first <a href="https://msdn.microsoft.com/ed1777bd-4c02-43e0-9bbb-6bb02702e1a4">MIB_IPADDRROW</a> array entry in the <b>table</b> member. Padding for alignment may also be present between the <b>MIB_IPADDRROW</b> array entries in the <b>table</b> member. Any access to a <b>MIB_IPADDRROW</b> array entry should assume  padding may exist. 



On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <a href="https://msdn.microsoft.com/ed1777bd-4c02-43e0-9bbb-6bb02702e1a4">MIB_IPADDRROW</a> is defined in the <i>Ipmib.h</i> header file not in the <i>Iprtrmib.h</i> header file. Note that the <i>Ipmib.h</i> header file is automatically included in <i>Iprtrmib.h</i> which is automatically included in the <i>Iphlpapi.h</i> header file. The <i>Ipmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.



#### Examples

The following example retrieves the IP address table, then prints some members of the IP address entries in the table.


```cpp
#include <winsock2.h>
#include <ws2tcpip.h>
#include <iphlpapi.h>
#include <stdio.h>

#pragma comment(lib, "iphlpapi.lib")
#pragma comment(lib, "ws2_32.lib")

#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x))
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))

/* Note: could also use malloc() and free() */

int __cdecl main()
{

    int i;
    
    /* Variables used by GetIpAddrTable */
    PMIB_IPADDRTABLE pIPAddrTable;
    DWORD dwSize = 0;
    DWORD dwRetVal = 0;
    IN_ADDR IPAddr;

    /* Variables used to return error message */
    LPVOID lpMsgBuf;

    // Before calling AddIPAddress we use GetIpAddrTable to get
    // an adapter to which we can add the IP.
    pIPAddrTable = (MIB_IPADDRTABLE *) MALLOC(sizeof (MIB_IPADDRTABLE));

    if (pIPAddrTable) {
        // Make an initial call to GetIpAddrTable to get the
        // necessary size into the dwSize variable
        if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) ==
            ERROR_INSUFFICIENT_BUFFER) {
            FREE(pIPAddrTable);
            pIPAddrTable = (MIB_IPADDRTABLE *) MALLOC(dwSize);

        }
        if (pIPAddrTable == NULL) {
            printf("Memory allocation failed for GetIpAddrTable\n");
            exit(1);
        }
    }
    // Make a second call to GetIpAddrTable to get the
    // actual data we want
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable failed with error %d\n", dwRetVal);
        if (FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM | FORMAT_MESSAGE_IGNORE_INSERTS, NULL, dwRetVal, MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),       // Default language
                          (LPTSTR) & lpMsgBuf, 0, NULL)) {
            printf("\tError: %s", lpMsgBuf);
            LocalFree(lpMsgBuf);
        }
        exit(1);
    }

    printf("\tNum Entries: %ld\n", pIPAddrTable->dwNumEntries);
    for (i=0; i < (int) pIPAddrTable->dwNumEntries; i++) {
        printf("\n\tInterface Index[%d]:\t%ld\n", i, pIPAddrTable->table[i].dwIndex);
        IPAddr.S_un.S_addr = (u_long) pIPAddrTable->table[i].dwAddr;
        printf("\tIP Address[%d]:     \t%s\n", i, inet_ntoa(IPAddr) );
        IPAddr.S_un.S_addr = (u_long) pIPAddrTable->table[i].dwMask;
        printf("\tSubnet Mask[%d]:    \t%s\n", i, inet_ntoa(IPAddr) );
        IPAddr.S_un.S_addr = (u_long) pIPAddrTable->table[i].dwBCastAddr;
        printf("\tBroadCast[%d]:      \t%s (%ld%)\n", i, inet_ntoa(IPAddr), pIPAddrTable->table[i].dwBCastAddr);
        printf("\tReassembly size[%d]:\t%ld\n", i, pIPAddrTable->table[i].dwReasmSize);
        printf("\tType and State[%d]:", i);
        if (pIPAddrTable->table[i].wType & MIB_IPADDR_PRIMARY)
            printf("\tPrimary IP Address");
        if (pIPAddrTable->table[i].wType & MIB_IPADDR_DYNAMIC)
            printf("\tDynamic IP Address");
        if (pIPAddrTable->table[i].wType & MIB_IPADDR_DISCONNECTED)
            printf("\tAddress is on disconnected interface");
        if (pIPAddrTable->table[i].wType & MIB_IPADDR_DELETED)
            printf("\tAddress is being deleted");
        if (pIPAddrTable->table[i].wType & MIB_IPADDR_TRANSIENT)
            printf("\tTransient address");
        printf("\n");
    }

    if (pIPAddrTable) {
        FREE(pIPAddrTable);
        pIPAddrTable = NULL;
    }

    exit(0);
}


```





## -see-also




<a href="https://msdn.microsoft.com/669264cd-a43c-4681-9416-2704d4232685">AddIPAddress</a>



<a href="https://msdn.microsoft.com/ec845db8-d544-4291-8221-0fde82c2de27">DisableMediaSense</a>



<a href="https://msdn.microsoft.com/7b34138f-7263-4b73-95df-9e854fd81135">GetAdaptersAddresses</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/a2df3749-6c75-40c0-8952-1656bbe639a6">IP_ADAPTER_ADDRESSES</a>



<a href="https://msdn.microsoft.com/ed1777bd-4c02-43e0-9bbb-6bb02702e1a4">MIB_IPADDRROW</a>



<a href="https://msdn.microsoft.com/12a929e5-813d-4dae-9ea0-5a3c0a88cf05">MIB_IPADDRTABLE</a>



<a href="https://msdn.microsoft.com/1a959da7-5fdb-4749-a4be-5d44e80ca2ea">RestoreMediaSense</a>
 

 

