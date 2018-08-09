---
UID: NF:iphlpapi.DeletePersistentTcpPortReservation
title: DeletePersistentTcpPortReservation function
author: windows-sdk-content
description: Deletes a persistent TCP port reservation for a consecutive block of TCP ports on the local computer.
old-location: iphlp\deletepersistenttcpportreservation.htm
old-project: iphlp
ms.assetid: 533F8B35-6EC1-43BB-B8E6-EB086A9C646C
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DeletePersistentTcpPortReservation, DeletePersistentTcpPortReservation function [IP Helper], iphlp.deletepersistenttcpportreservation, iphlpapi/DeletePersistentTcpPortReservation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: NET_ADDRESS_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - DeletePersistentTcpPortReservation
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include &lt;Windows.h.&gt;
#include &lt;winsock2.h&gt;
#include &lt;ws2ipdef.h&gt; 
#include &lt;iphlpapi.h&gt;
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

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
        wprintf(L"usage: %s &lt;Starting Port&gt; &lt;Number of Ports&gt;\n", argv[0]);
        wprintf(L"Delete a persistent TCP port reservation\n");
        wprintf(L"Example usage:\n");
        wprintf(L"   %s 5000 20\n", argv[0]);
        wprintf(L"   where StartPort=5000 NumPorts=20");
        return 1;
    }

    startPort = _wtoi(argv[1]);
    if ( startPort &lt; 0 || startPort&gt; 65535) {
        wprintf(L"Starting point must be either 0 or between 1 and 65,535\n");
        return 1;
    }    
    startPortns = htons((u_short) startPort);

    numPorts = _wtoi(argv[2]);
    if (numPorts &lt; 0) {
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/19DAF828-B0E4-49E2-843D-7350C8083C45">CreatePersistentTcpPortReservation</a>



<a href="https://msdn.microsoft.com/AFD2EFD1-55AF-49C9-8109-D4D1B7BB7C94">CreatePersistentUdpPortReservation</a>



<a href="https://msdn.microsoft.com/E6539B3F-48DA-41AA-8AD4-2EBBAF98069F">DeletePersistentUdpPortReservation</a>



<a href="https://msdn.microsoft.com/5EBEB774-13A2-49C2-92ED-5271081615AA">LookupPersistentTcpPortReservation</a>



<a href="https://msdn.microsoft.com/621C732E-9A42-455C-A1A8-F1997D6EF0D7">LookupPersistentUdpPortReservation</a>
 

 

