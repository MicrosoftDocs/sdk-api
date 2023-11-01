---
UID: NF:iphlpapi.RestoreMediaSense
title: RestoreMediaSense function (iphlpapi.h)
description: The RestoreMediaSense function restores the media sensing capability of the TCP/IP stack on a local computer on which the DisableMediaSense function was previously called.
helpviewer_keywords: ["RestoreMediaSense","RestoreMediaSense function [IP Helper]","iphlp.restoremediasense","iphlpapi/RestoreMediaSense"]
old-location: iphlp\restoremediasense.htm
tech.root: IpHlp
ms.assetid: 1a959da7-5fdb-4749-a4be-5d44e80ca2ea
ms.date: 12/05/2018
ms.keywords: RestoreMediaSense, RestoreMediaSense function [IP Helper], iphlp.restoremediasense, iphlpapi/RestoreMediaSense
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
 - RestoreMediaSense
 - iphlpapi/RestoreMediaSense
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
 - RestoreMediaSense
---

# RestoreMediaSense function


## -description

The <b>RestoreMediaSense</b> function restores the media sensing capability of the TCP/IP stack on a local computer on which the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-disablemediasense">DisableMediaSense</a> function was previously called.

## -parameters

### -param pOverlapped

A pointer to an 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. Except for the <b>hEvent</b> member, all members of this structure must be set to zero. The <b>hEvent</b> member should contain a handle to a valid event object. Use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function to create this event object.

### -param lpdwEnableCount [optional]

An optional pointer to a DWORD variable that receives the number of references remaining if the <b>RestoreMediaSense</b> function succeeds. The variable is also used by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-enablerouter">EnableRouter</a> and <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-unenablerouter">UnenableRouter</a> functions.

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
An invalid parameter was passed to the function. This error is returned if an <i>pOverlapped</i> parameter is a bad pointer.  This error is also returned if the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-disablemediasense">DisableMediaSense</a> function was not called prior to calling the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-restoremediasense">RestoreMediaSense</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_IO_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The operation is in progress. This value may be returned by a successful asynchronous call to <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-restoremediasense">RestoreMediaSense</a>.  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OPEN_FAILED</b></dt>
</dl>
</td>
<td width="60%">
An internal handle to the driver was invalid. 

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

If the <i>pOverlapped</i> parameter is <b>NULL</b>, the <b>RestoreMediaSense</b> function is  executed synchronously. 

If the <i>pOverlapped</i> parameter is not <b>NULL</b>, the <b>RestoreMediaSense</b> function is  executed asynchronously using the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure pointed to by the <i>pOverlapped</i> parameter. 

The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-disablemediasense">DisableMediaSense</a> function does not complete until the <b>RestoreMediaSense</b> function is called later to restore the media sensing capability. Until then, an I/O request packet (IRP) remains queued up. Alternatively, when the process that called <b>DisableMediaSense</b> exits, the IRP is canceled and a cancel routine is called that would again restore the media sensing capability. 


To call <b>RestoreMediaSense</b> synchronously, an application needs to pass a <b>NULL</b> pointer in the <i>pOverlapped</i> parameter. When <b>RestoreMediaSense</b> is called synchronously, the function returns when the I/O request packet (IRP) to restore the media sense has completed. 

To call <b>RestoreMediaSense</b> asynchronously, an application needs to allocate an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. Except for the <b>hEvent</b> member, all members of this structure must be set to zero. The <b>hEvent</b> member requires a handle to a valid event object. Use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function to create this event. When called asynchronously, <b>RestoreMediaSense</b> can return ERROR_IO_PENDING. The IRP completes when the media sensing capability has been restored. Use the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle to the event object when it is no longer needed. The system closes the handle automatically when the process terminates. The event object is destroyed when its last handle has been closed. 

If <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-disablemediasense">DisableMediaSense</a> was not called prior to calling <b>RestoreMediaSense</b>, then <b>RestoreMediaSense</b> returns ERROR_INVALID_PARAMETER.

On Windows Server 2003and Windows XP, the TCP/IP stack implements a policy of deleting all IP addresses on an interface in response to a media sense disconnect event from an underlying network interface. If a network switch or hub that the local computer is connected to is powered off, or a network cable is disconnected, the network interface will deliver disconnection events. IP configuration information associated with the network interface is lost. As a result, the TCP/IP stack implements a policy of hiding disconnected interfaces so these interfaces and their associated IP addresses do not show up in configuration information retrieved through IP helper. This policy prevents some applications from easily detecting that a network interface is merely disconnected, rather than removed from the system.

This behavior does not normally impact a local client computer if it is using DHCP requests to a DHCP server for IP configuration information. But this can have a serious impact on server computers, particularly computers used as part of clusters. The <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-disablemediasense">DisableMediaSense</a> function can be used to temporarily disable the media sense capability for these cases. At some later time, the <b>RestoreMediaSense</b> function would be called to restore the media sensing capability.

The following registry setting is related to the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-disablemediasense">DisableMediaSense</a> and <b>RestoreMediaSense</b> functions:


<b>System</b>&#92;<b>CurrentControlSet</b>&#92;<b>Services</b>&#92;<b>Tcpip</b>&#92;<b>Parameters</b>&#92;<b>DisableDHCPMediaSense</b>



There is an internal flag in Windows that is set if this registry key exists when the machine first boots up. The same internal flag also gets set and reset by calling <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-disablemediasense">DisableMediaSense</a> and <b>RestoreMediaSense</b>. However with registry setting, you need to reboot the machine for the changes to take place.


The TCP/IP stack on Windows Vista and later was changed to not hide disconnected interfaces when a disconnect event occurs. So on Windows Vista and later, the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-disablemediasense">DisableMediaSense</a> and <b>RestoreMediaSense</b> functions don't do anything and always returns NO_ERROR.


#### Examples

The following example shows how to call the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-disablemediasense">DisableMediaSense</a> and <b>RestoreMediaSense</b> functions synchronously. This sample is only useful on Windows Server 2003and Windows XP where the <b>DisableMediaSense</b> and <b>RestoreMediaSense</b> functions do something useful.

The sample first creates a separate thread that calls the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-disablemediasense">DisableMediaSense</a> function synchronously, the main thread sleeps for 60 seconds to allow the user to disconnect a network cable, retrieves the IP address table and prints some members of the IP address entries in the table, calls the <b>RestoreMediaSense</b> function synchronously, retrieves the IP address table again, and prints some members of the IP address entries in the table.  The impact of disabling the media sensing capability can be seen in the difference in the IP address table entries. 

For an example that shows how to call the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-disablemediasense">DisableMediaSense</a> and <b>RestoreMediaSense</b> functions asynchronously, see the <b>DisableMediaSense</b> function reference.


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

// The thread proc to call DisableMediaSense
DWORD WINAPI ThreadProc(LPVOID lpParam)
{
    if (*((DWORD *) lpParam)) {
        DWORD dwRetVal;
        dwRetVal = DisableMediaSense(NULL, NULL);
        if (dwRetVal && dwRetVal != ERROR_IO_PENDING) {
            printf("DisableMediaSense failed with error %d\n", dwRetVal);
            return 0;
        } else {
            Sleep(1000);
            printf(" === DisableMediaSense Returned now. ===\n\n");
        }
    }
    return 0;
}

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

    /* Variable to use with RestoreMediaSense */
    DWORD dwEnableCount = 0;

    // Variables used to create a separate thread to call
    // the DisableMediaSense function
    DWORD ThreadID;
    DWORD IsDisable = TRUE;
    HANDLE Disable_THandle;

    // Create the thread to call Disable MediaSense synchronously
    Disable_THandle =
        CreateThread(NULL, 0, ThreadProc, (LPVOID) & IsDisable, 0, &ThreadID);
    if (!Disable_THandle) {
        printf("CreateTread Failed:%d", GetLastError());
        exit(1);
    }

    printf(" === DisableMediaSense called on separate thread ===\n\n");
// Sleep for 60 seconds so we can disconnect a cable
    Sleep(60000);

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

    // Call RestoreMediaSense synchronously to enable mediasense
    dwRetVal = RestoreMediaSense(NULL, &dwEnableCount);
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



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-disablemediasense">DisableMediaSense</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-enablerouter">EnableRouter</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-unenablerouter">UnenableRouter</a>