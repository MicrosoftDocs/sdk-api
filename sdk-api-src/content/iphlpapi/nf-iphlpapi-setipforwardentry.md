---
UID: NF:iphlpapi.SetIpForwardEntry
title: SetIpForwardEntry function (iphlpapi.h)
description: The SetIpForwardEntry function modifies an existing route in the local computer's IPv4 routing table.
helpviewer_keywords: ["SetIpForwardEntry","SetIpForwardEntry function [IP Helper]","_iphlp_setipforwardentry","iphlp.setipforwardentry","iphlpapi/SetIpForwardEntry"]
old-location: iphlp\setipforwardentry.htm
tech.root: IpHlp
ms.assetid: a98de796-8fa2-4835-8d15-07d86d89c348
ms.date: 12/05/2018
ms.keywords: SetIpForwardEntry, SetIpForwardEntry function [IP Helper], _iphlp_setipforwardentry, iphlp.setipforwardentry, iphlpapi/SetIpForwardEntry
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
 - SetIpForwardEntry
 - iphlpapi/SetIpForwardEntry
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
 - SetIpForwardEntry
---

# SetIpForwardEntry function


## -description

The 
<b>SetIpForwardEntry</b> function modifies an existing route in the local computer's IPv4 routing table.

## -parameters

### -param pRoute [in]

A pointer to a 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a> structure that specifies the new information for the existing route. The caller must specify <b>MIB_IPPROTO_NETMGMT</b> for the <b>dwForwardProto</b> member of this structure. The caller must also specify values for the <b>dwForwardIfIndex</b>, <b>dwForwardDest</b>, <b>dwForwardMask</b>, <b>dwForwardNextHop</b>, and <b>dwForwardPolicy</b> members of the structure.

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
Access is denied. This error is returned on Windows Vista and Windows Server 2008 under several conditions that include the following: the  user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (RunAs administrator).  

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The system cannot find the file specified. This error is returned on Windows Vista and later if the  network interface specified by the <b>dwForwardIfIndex</b>  member of the <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a> structure pointed to by the <i>pRoute</i> parameter could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pRoute</i> parameter is <b>NULL</b>, or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipforwardentry">SetIpForwardEntry</a> is unable to read from the memory pointed to by <i>pRoute</i>, or one of the members of the 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a> structure is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The element is not found. The error is returned on Windows Vista and later when the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipforwardentry">DeleteIpForwardEntry</a> function and then the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-setipforwardentry">SetIpForwardEntry</a> function are called for the same IPv4 route table entry. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This value is returned if the IPv4 transport is not configured on the local computer. This error is also returned on Windows Server 2003 and earlier if no TCP/IP stack is configured on the local computer.  

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

The <b>dwForwardProto</b> member of 
<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a> structure pointed to by the <i>route</i> parameter must be set to <b>MIB_IPPROTO_NETMGMT</b> otherwise <b>SetIpForwardEntry</b> will fail. Routing protocol identifiers are used to identify route information for the specified routing protocol. For example, <b>MIB_IPPROTO_NETMGMT</b> is used to identify route information for IP  routing set through network management such as the Dynamic Host Configuration Protocol (DHCP), the Simple Network Management Protocol (SNMP), or by calls to the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createipforwardentry">CreateIpForwardEntry</a>,  <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipforwardentry">DeleteIpForwardEntry</a>, or <b>SetIpForwardEntry</b> functions.

On Windows Vista and Windows Server 2008, the route metric specified in the <b>dwForwardMetric1</b> member of the  <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a> structure pointed to by <i>pRoute</i> parameter represents a combination of the route metric added to the interface metric specified in the <b>Metric</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a> structure of the associated interface.  So the <b>dwForwardMetric1</b> member of the  <b>MIB_IPFORWARDROW</b> structure should be equal to or greater than <b>Metric</b> member of the associated <b>MIB_IPINTERFACE_ROW</b> structure. If an application would like to set the route metric to 0, then the <b>dwForwardMetric1</b> member of the <b>MIB_IPFORWARDROW</b> structure  should be set equal to the value of the interface metric specified in the <b>Metric</b> member of the associated <b>MIB_IPINTERFACE_ROW</b> structure. An application can retrieve the interface metric by calling the <a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfaceentry">GetIpInterfaceEntry</a> function.

On Windows Vista and Windows Server 2008, the <b>SetIpForwardEntry</b> function only works on interfaces with a single sub-interface (where the interface LUID and subinterface LUID are the same). The <b>dwForwardIfIndex</b> member of the <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a> structure specifies the interface.

The <b>dwForwardAge</b> member the <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a> structure  pointed to by the <i>route</i> parameter is not currently used by <b>SetIpForwardEntry</b>. The <b>dwForwardAge</b> member is used only if the Routing and Remote Access Service (RRAS)is running, and then only for routes of type <b>MIB_IPPROTO_NETMGMT</b> as defined on the <a href="/windows/desktop/RRAS/protocol-identifiers">Protocol Identifiers</a> reference page. When <b>dwForwardAge</b> is set to <b>INFINITE</b>, the route will not be removed based on a timeout
 
value. Any other value for <b>dwForwardAge</b> specifies the number of seconds until the TCP/IP stack will remove the route from the network routing table.

A route modified by <b>SetIpForwardEntry</b> will automatically have a default value for <b>dwForwardAge</b> of INFINITE.

A number of members of the <a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a> structure  pointed to by the <i>route</i> parameter are not currently used by <b>SetIpForwardEntry</b>. These members include <b>dwForwardPolicy</b>, <b>dwForwardType</b>, <b>dwForwardAge</b>, <b>dwForwardNextHopAS</b>, <b>dwForwardMetric1</b>, <b>dwForwardMetric2</b>, <b>dwForwardMetric3</b>, <b>dwForwardMetric4</b>, and <b>dwForwardMetric5</b>. 

To create a new route in the IP routing table, use the 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createipforwardentry">CreateIpForwardEntry</a> function. To retrieve the IP routing table, call the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipforwardtable">GetIpForwardTable</a> function.

On Windows Vista and later, the <b>SetIpForwardEntry</b> function can only be called by a user logged on as a member of the Administrators group. If <b>SetIpForwardEntry</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. 

This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.



<div class="alert"><b>Note</b>  On Windows NT 4.0 and Windows 2000 and later, this function executes a privileged operation. For this function to execute successfully, the caller must be logged on as a member of the Administrators group or the NetworkConfigurationOperators group.</div>
<div> </div>

#### Examples

The following example demonstrates how to change the default gateway to NewGateway. Simply calling <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipforwardtable">GetIpForwardTable</a>, changing the gateway and then calling <b>SetIpForwardEntry</b> will not change the route, but rather will just add a new one. If for some reason there are multiple default gateways present, this code will delete them. Note that the new gateway must be viable; otherwise, TCP/IP will ignore the change.




<div class="alert"><b>Note</b>  Executing this code will change your IP routing tables and will likely cause network activity to fail.</div>
<div> </div>



<b>Windows Vista and later:  </b>When the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipforwardentry">DeleteIpForwardEntry</a> function and then <b>SetIpForwardEntry</b> function are called for the same route table entry on Windows Vista and later, ERROR_NOT_FOUND is returned. The proper way to replicate this example on Windows Vista and later is to use the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createipforwardentry">CreateIpForwardEntry</a> function to create the new route table entry and then delete the old route table entry by calling the <b>DeleteIpForwardEntry</b> function.






```cpp
#pragma comment(lib, "IPHLPAPI.lib")

// #ifndef WIN32_LEAN_AND_MEAN
// #define WIN32_LEAN_AND_MEAN
// #endif

// #pragma warning(push)
// #pragma warning(disable: 4127)

// #include <windows.h>

#include <winsock2.h>
#include <ws2tcpip.h>
#include <iphlpapi.h>
#include <stdio.h>

#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x))
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))
/* Note: could also use malloc() and free() */

int main()
{

    // Declare and initialize variables.

    /* variables used for SetIfForwardEntry */

    PMIB_IPFORWARDTABLE pIpForwardTable = NULL;
    PMIB_IPFORWARDROW pRow = NULL;
    DWORD dwSize = 0;
    BOOL bOrder = FALSE;
    DWORD dwStatus = 0;
    DWORD NewGateway = 0xDDBBCCAA;      // this is in host order Ip Address AA.BB.CC.DD is DDCCBBAA
    DWORD i;

// Find out how big our buffer needs to be.
    dwStatus = GetIpForwardTable(pIpForwardTable, &dwSize, bOrder);
    if (dwStatus == ERROR_INSUFFICIENT_BUFFER) {
        // Allocate the memory for the table
        pIpForwardTable = (PMIB_IPFORWARDTABLE) malloc(dwSize);
        if (pIpForwardTable == NULL) {
            printf("Unable to allocate memory for the IPFORWARDTALE\n");
            exit(1);
        }
        // Now get the table.
        dwStatus = GetIpForwardTable(pIpForwardTable, &dwSize, bOrder);
    }

    if (dwStatus != ERROR_SUCCESS) {
        printf("getIpForwardTable failed.\n");
        if (pIpForwardTable)
            free(pIpForwardTable);
        exit(1);
    }
// Search for the row in the table we want. The default gateway has a destination
// of 0.0.0.0. Notice that we continue looking through the table, but copy only
// one row. This is so that if there happen to be multiple default gateways, we can
// be sure to delete them all.
    for (i = 0; i < pIpForwardTable->dwNumEntries; i++) {
        if (pIpForwardTable->table[i].dwForwardDest == 0) {
            // We have found the default gateway.
            if (!pRow) {
                // Allocate some memory to store the row in. This is easier than filling
                // in the row structure ourselves, and we can be sure to change only the
                // gateway address.
                pRow = (PMIB_IPFORWARDROW) malloc(sizeof (MIB_IPFORWARDROW));
                if (!pRow) {
                    printf("Malloc failed. Out of memory.\n");
                    exit(1);
                }
                // Copy the row.
                memcpy(pRow, &(pIpForwardTable->table[i]),
                       sizeof (MIB_IPFORWARDROW));
            }
            // Delete the old default gateway entry.
            dwStatus = DeleteIpForwardEntry(&(pIpForwardTable->table[i]));

            if (dwStatus != ERROR_SUCCESS) {
                printf("Could not delete old gateway\n");
                exit(1);
            }
        }
    }

// Set the nexthop field to our new gateway. All the other properties of the route will
// be the same as they were previously.
    pRow->dwForwardNextHop = NewGateway;

// Create a new route entry for the default gateway.
    dwStatus = SetIpForwardEntry(pRow);

    if (dwStatus == NO_ERROR)
        printf("Gateway changed successfully\n");
    else if (dwStatus == ERROR_INVALID_PARAMETER)
        printf("Invalid parameter.\n");
    else
        printf("Error: %d\n", dwStatus);

// Free resources.
    if (pIpForwardTable)
        free(pIpForwardTable);
    if (pRow)
        free(pRow);
}


```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-createipforwardentry">CreateIpForwardEntry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipforwardentry">DeleteIpForwardEntry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipforwardtable">GetIpForwardTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfaceentry">GetIpInterfaceEntry</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/ipmib/ns-ipmib-mib_ipforwardrow">MIB_IPFORWARDROW</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a>