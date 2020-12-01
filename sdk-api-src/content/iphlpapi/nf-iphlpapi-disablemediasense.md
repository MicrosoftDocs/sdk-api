---
UID: NF:iphlpapi.DisableMediaSense
title: DisableMediaSense function (iphlpapi.h)
description: The DisableMediaSense function disables the media sensing capability of the TCP/IP stack on a local computer.
helpviewer_keywords: ["DisableMediaSense","DisableMediaSense function [IP Helper]","iphlp.disablemediasense","iphlpapi/DisableMediaSense"]
old-location: iphlp\disablemediasense.htm
tech.root: IpHlp
ms.assetid: ec845db8-d544-4291-8221-0fde82c2de27
ms.date: 12/05/2018
ms.keywords: DisableMediaSense, DisableMediaSense function [IP Helper], iphlp.disablemediasense, iphlpapi/DisableMediaSense
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - DisableMediaSense
 - iphlpapi/DisableMediaSense
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
 - DisableMediaSense
---

# DisableMediaSense function


## -description

The <b>DisableMediaSense</b> function disables the media sensing capability of the TCP/IP stack on a local computer.

## -parameters

### -param pHandle

A pointer to a variable that is used to store a handle. If the <i>pOverlapped</i> parameter is not <b>NULL</b>, this variable will be used internally to store a handle required to call the IP driver and disable the media sensing capability.

An application should not use the value pointed to by this variable. This handle is for internal use and should not be closed.

### -param pOverLapped

A pointer to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. Except for the <b>hEvent</b> member, all members of this structure must be set to zero. The <b>hEvent</b> member requires a handle to a valid event object. Use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function to create this event object.

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
An invalid parameter was passed to the function. This error is returned if an <i>pOverlapped</i> parameter is a bad pointer.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The operation is in progress. This value is returned by a successful asynchronous call to <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-disablemediasense">DisableMediaSense</a>.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OPEN_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The handle pointed to by the <i>pHandle</i> parameter was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. 

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

If the <i>pHandle</i> or <i>pOverlapped</i> parameters are <b>NULL</b>, the <b>DisableMediaSense</b> function is  executed synchronously. 

If both the <i>pHandle</i> and  <i>pOverlapped</i> parameters are not <b>NULL</b>, the <b>DisableMediaSense</b> function is  executed asynchronously using the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure pointed to by the <i>pOverlapped</i> parameter. 

The <b>DisableMediaSense</b> function does not complete until the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-restoremediasense">RestoreMediaSense</a> function is called later to restore the media sensing capability. Until then, an I/O request packet (IRP) remains queued up. Alternatively, when the process that called <b>DisableMediaSense</b> exits, the IRP is canceled and a cancel routine is called that would again restore the media sensing capability. 


To call <b>DisableMediaSense</b> synchronously, an application needs to create a separate thread for this call. Otherwise it would keep waiting for IRP completion and the function will block. 

To call <b>DisableMediaSense</b> asynchronously, an application needs to allocate an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. Except for the <b>hEvent</b> member, all members of this structure must be set to zero. The <b>hEvent</b> member requires a handle to a valid event object. Use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function to create this event. When called asynchronously, <b>DisableMediaSense</b> always returns ERROR_IO_PENDING. The IRP will be completed only when <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-restoremediasense">RestoreMediaSense</a> is called later.   Use the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle to the event object when it is no longer needed. The system closes the handle automatically when the process terminates. The event object is destroyed when its last handle has been closed. 

On Windows Server 2003and Windows XP, the TCP/IP stack implements a policy of deleting all IP addresses on an interface in response to a media sense disconnect event from an underlying network interface. If a network switch or hub that the local computer is connected to is powered off, or a network cable is disconnected, the network interface will deliver disconnection events. IP configuration information associated with the network interface is lost. As a result, the TCP/IP stack implements a policy of hiding disconnected interfaces so these interfaces and their associated IP addresses do not show up in configuration information retrieved through IP helper. This policy prevents some applications from easily detecting that a network interface is merely disconnected, rather than removed from the system.

This behavior does not normally impact a local client computer if it is using DHCP requests to a DHCP server for IP configuration information. But this can have a serious impact on server computers, particularly computers used as part of clusters. The <b>DisableMediaSense</b> function can be used to temporarily disable the media sensing capability for these cases. At some later time, the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-restoremediasense">RestoreMediaSense</a> function would be called to restore the media sensing capability.

The following registry setting is related to the <b>DisableMediaSense</b> and <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-restoremediasense">RestoreMediaSense</a> functions:


<b>System</b>&#92;<b>CurrentControlSet</b>&#92;<b>Services</b>&#92;<b>Tcpip</b>&#92;<b>Parameters</b>&#92;<b>DisableDHCPMediaSense</b>



There is an internal flag in Windows that is set if this registry key exists when the machine first boots up. The same internal flag also gets set and reset by calling <b>DisableMediaSense</b> and <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-restoremediasense">RestoreMediaSense</a>. However with registry setting, you need to reboot the machine for the changes to take place.


The TCP/IP stack on Windows Vista and later was changed to not hide disconnected interfaces when a disconnect event occurs. So on Windows Vista and later, the <b>DisableMediaSense</b> and <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-restoremediasense">RestoreMediaSense</a> functions don't do anything and always returns NO_ERROR.


#### Examples

The following example shows how to call the <b>DisableMediaSense</b> and <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-restoremediasense">RestoreMediaSense</a> functions asynchronously. This sample is only useful on Windows Server 2003and Windows XP where the <b>DisableMediaSense</b> and <b>RestoreMediaSense</b> functions do something useful.

The sample first calls the <b>DisableMediaSense</b> function, sleeps for 60 seconds to allow the user to disconnect a network cable, retrieves the IP address table and prints some members of the IP address entries in the table, calls the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-restoremediasense">RestoreMediaSense</a> function, retrieves the IP address table again, and prints some members of the IP address entries in the table.  The impact of disabling the media sensing capability can be seen in the difference in the IP address table entries. 

For an example that shows how to call the <b>DisableMediaSense</b> and <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-restoremediasense">RestoreMediaSense</a> functions synchronously, see the <b>RestoreMediaSense</b> function reference.


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

    // Variables to call DisableMediaSense
    //  and RestoreMediaSense asynchronously
    HANDLE IpDriverHandle = INVALID_HANDLE_VALUE;
    OVERLAPPED Overlapped;
    HANDLE DriverHandle;
    DWORD dwEnableCount = 0;

    memset(&Overlapped, 0, sizeof (Overlapped));
    Overlapped.hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);

    dwRetVal = DisableMediaSense(&DriverHandle, &Overlapped);
    if (dwRetVal != ERROR_IO_PENDING) {
        printf("DisableMediaSense failed with error %d\n", dwRetVal);
        exit(1);
    } else {
        printf(" === DisableMediaSense called ===\n\n");
        // Sleep for 60 seconds so we can disconnect a cable
        Sleep(60000);
    }

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
    if ((dwRetVal = GetIpAddrTable(pIPAddrTable, &dwSize, 0)) != NO_ERROR) {
        printf("GetIpAddrTable failed with error %d\n", dwRetVal);
        if (FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER |
                    FORMAT_MESSAGE_FROM_SYSTEM | FORMAT_MESSAGE_IGNORE_INSERTS, 
                    NULL, 
                    dwRetVal, 
                    MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), // Default language
                    (LPTSTR) & lpMsgBuf, 0, NULL)) {
            printf("\tError: %s", lpMsgBuf);
            LocalFree(lpMsgBuf);
        }
        exit(1);
    }

    printf("\tNum Entries: %ld\n", pIPAddrTable->dwNumEntries);
    for (i = 0; i < (int) pIPAddrTable->dwNumEntries; i++) {
        printf("\n\tInterface Index[%d]:\t%ld\n", i,
               pIPAddrTable->table[i].dwIndex);
        IPAddr.S_un.S_addr = (u_long) pIPAddrTable->table[i].dwAddr;
        printf("\tIP Address[%d]:     \t%s\n", i, inet_ntoa(IPAddr));
        IPAddr.S_un.S_addr = (u_long) pIPAddrTable->table[i].dwMask;
        printf("\tSubnet Mask[%d]:    \t%s\n", i, inet_ntoa(IPAddr));
        IPAddr.S_un.S_addr = (u_long) pIPAddrTable->table[i].dwBCastAddr;
        printf("\tBroadCast[%d]:      \t%s (%ld%)\n", i, inet_ntoa(IPAddr),
               pIPAddrTable->table[i].dwBCastAddr);
        printf("\tReassembly size[%d]:\t%ld\n", i,
               pIPAddrTable->table[i].dwReasmSize);
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

    // Call RestoreMediaSense asynchronously to enable mediasense
    dwRetVal = RestoreMediaSense(&Overlapped, &dwEnableCount);
    if (dwRetVal && dwRetVal != ERROR_IO_PENDING) {
        printf("RestoreMediaSense failed with error %d\n", dwRetVal);
        exit(1);
    } else {
        printf(" === RestoreMediaSense called ===\n");
        printf("  EnableCount returned was %ld\n\n", dwEnableCount);
    }

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
    if ((dwRetVal = GetIpAddrTable(pIPAddrTable, &dwSize, 0)) != NO_ERROR) {
        printf("GetIpAddrTable failed with error %d\n", dwRetVal);
        if (FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER | 
                    FORMAT_MESSAGE_FROM_SYSTEM | FORMAT_MESSAGE_IGNORE_INSERTS, 
                    NULL, dwRetVal, 
                    MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),  // Default language
                    (LPTSTR) & lpMsgBuf, 0, NULL)) {
            printf("\tError: %s", lpMsgBuf);
            LocalFree(lpMsgBuf);
        }
        exit(1);
    }

    printf("\tNum Entries: %ld\n", pIPAddrTable->dwNumEntries);
    for (i = 0; i < (int) pIPAddrTable->dwNumEntries; i++) {
        printf("\n\tInterface Index[%d]:\t%ld\n", i,
               pIPAddrTable->table[i].dwIndex);
        IPAddr.S_un.S_addr = (u_long) pIPAddrTable->table[i].dwAddr;
        printf("\tIP Address[%d]:     \t%s\n", i, inet_ntoa(IPAddr));
        IPAddr.S_un.S_addr = (u_long) pIPAddrTable->table[i].dwMask;
        printf("\tSubnet Mask[%d]:    \t%s\n", i, inet_ntoa(IPAddr));
        IPAddr.S_un.S_addr = (u_long) pIPAddrTable->table[i].dwBCastAddr;
        printf("\tBroadCast[%d]:      \t%s (%ld%)\n", i, inet_ntoa(IPAddr),
               pIPAddrTable->table[i].dwBCastAddr);
        printf("\tReassembly size[%d]:\t%ld\n", i,
               pIPAddrTable->table[i].dwReasmSize);
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

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-enablerouter">EnableRouter</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-restoremediasense">RestoreMediaSense</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-unenablerouter">UnenableRouter</a>