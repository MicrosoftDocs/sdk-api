---
UID: NF:iphlpapi.DeletePersistentTcpPortReservation
title: DeletePersistentTcpPortReservation function (iphlpapi.h)
description: Deletes a persistent TCP port reservation for a consecutive block of TCP ports on the local computer. (DeletePersistentTcpPortReservation)
helpviewer_keywords: ["DeletePersistentTcpPortReservation","DeletePersistentTcpPortReservation function [IP Helper]","iphlp.deletepersistenttcpportreservation","iphlpapi/DeletePersistentTcpPortReservation"]
old-location: iphlp\deletepersistenttcpportreservation.htm
tech.root: IpHlp
ms.assetid: 533F8B35-6EC1-43BB-B8E6-EB086A9C646C
ms.date: 12/05/2018
ms.keywords: DeletePersistentTcpPortReservation, DeletePersistentTcpPortReservation function [IP Helper], iphlp.deletepersistenttcpportreservation, iphlpapi/DeletePersistentTcpPortReservation
req.header: iphlpapi.h
req.include-header: 
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DeletePersistentTcpPortReservation
 - iphlpapi/DeletePersistentTcpPortReservation
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
 - DeletePersistentTcpPortReservation
---

# DeletePersistentTcpPortReservation function


## -description

The 
<b>DeletePersistentTcpPortReservation</b> function deletes a persistent TCP port reservation for a consecutive block of TCP ports on the local computer.

## -parameters

### -param StartPort [in]

The starting TCP port number in network byte order.

### -param NumberOfPorts [in]

The number of TCP port numbers to delete.

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
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. This error is returned under several conditions that include the following: the  user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (RunAs administrator).  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if zero is passed in the <i>StartPort</i>  or <i>NumberOfPorts</i> parameters. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The element was not found. This error is returned if persistent port block specified by the <i>StartPort</i>  and <i>NumberOfPorts</i> parameters could not be found. 

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

The <b>DeletePersistentTcpPortReservation</b> function is defined on Windows Vista and later. 

The <b>DeletePersistentTcpPortReservation</b> function is used to delete a persistent reservation for a block of TCP ports. 

The <b>DeletePersistentTcpPortReservation</b> function can only be called by a user logged on as a member of the Administrators group. If <b>DeletePersistentTcpPortReservation</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.




#### Examples

The following example deletes a persistent TCP port reservation. 

This example must be run by a user that is a member of the Administrators group. The simplest way to run this example is in an enhanced shell as the built-in Administrator (RunAs administrator). 


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h.>
#include <winsock2.h>
#include <ws2ipdef.h> 
#include <iphlpapi.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with iphlpapi.lib
#pragma comment(lib, "iphlpapi.lib")

// Need to link with ws2_32.lib for htons
#pragma comment(lib, "ws2_32.lib")

int wmain(int argc, WCHAR **argv)  {

    // Declare and initialize variables
    
    int startPort = 0;         // host byte order
    int numPorts = 0;
    USHORT startPortns = 0;    // Network byte order
    
    unsigned long status = 0;

    // Validate the parameters
    if (argc != 3) {
        wprintf(L"usage: %s <Starting Port> <Number of Ports>\n", argv[0]);
        wprintf(L"Delete a persistent TCP port reservation\n");
        wprintf(L"Example usage:\n");
        wprintf(L"   %s 5000 20\n", argv[0]);
        wprintf(L"   where StartPort=5000 NumPorts=20");
        return 1;
    }

    startPort = _wtoi(argv[1]);
    if ( startPort < 0 || startPort> 65535) {
        wprintf(L"Starting point must be either 0 or between 1 and 65,535\n");
        return 1;
    }    
    startPortns = htons((u_short) startPort);

    numPorts = _wtoi(argv[2]);
    if (numPorts < 0) {
        wprintf(L"Number of ports must be a positive number\n");
        return 1;
    }    

    status = DeletePersistentTcpPortReservation((USHORT) startPortns, (USHORT) numPorts);
    if( status != NO_ERROR )
    {
        wprintf(L"DeletePersistentTcpPortReservation returned error: %ld\n", 
            status);
        return 1;
    }

    wprintf(L"DeletePersistentTcpPortReservation call succeeded\n");  

    return 0;
}

```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation">CreatePersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation">CreatePersistentUdpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation">DeletePersistentUdpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation">LookupPersistentTcpPortReservation</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation">LookupPersistentUdpPortReservation</a>
