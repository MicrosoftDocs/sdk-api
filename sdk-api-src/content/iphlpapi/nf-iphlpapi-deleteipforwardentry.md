---
UID: NF:iphlpapi.DeleteIpForwardEntry
title: DeleteIpForwardEntry function
author: windows-sdk-content
description: Deletes an existing route in the local computer's IPv4 routing table.
old-location: iphlp\deleteipforwardentry.htm
tech.root: iphlp
ms.assetid: 70bcfd71-34dd-465d-890b-1dd829632fb0
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: DeleteIpForwardEntry, DeleteIpForwardEntry function [IP Helper], _iphlp_deleteipforwardentry, iphlp.deleteipforwardentry, iphlpapi/DeleteIpForwardEntry
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
 - DeleteIpForwardEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeleteIpForwardEntry function


## -description


The 
<b>DeleteIpForwardEntry</b> function deletes an existing route in the local computer's IPv4 routing table.


## -parameters




### -param pRoute [in]

A pointer to an 
<a href="https://msdn.microsoft.com/ff451481-3e9d-4add-94e2-846d67002a38">MIB_IPFORWARDROW</a> structure. This structure specifies information that identifies the route to delete. The caller must specify values for the <b>dwForwardIfIndex</b>, <b>dwForwardDest</b>, <b>dwForwardMask</b>, <b>dwForwardNextHop</b>,  and <b>dwForwardProto</b> members of the structure.


## -returns



The function returns <b>NO_ERROR</b> (zero) if the routine is successful. 

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Error code</th>
<th>Meaning</th>
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
<dt><b> ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An input parameter is invalid, no action was taken. This error is returned if the <b>pRoute</b> parameter is <b>NULL</b>, the <b>dwForwardMask</b> member of the <a href="https://msdn.microsoft.com/ff451481-3e9d-4add-94e2-846d67002a38">PMIB_IPFORWARDROW</a> structure is not a valid IPv4 subnet mask, the <b>dwForwardIfIndex</b> member is <b>NULL</b>, or one of the other members of the 
<b>MIB_IPFORWARDROW</b> structure is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The <b>pRoute</b> parameter points to a route entry that does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The IPv4 transport is not configured on the local computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>(other)</b></dt>
</dl>
</td>
<td width="60%">
The function may return other error codes.

</td>
</tr>
</table>
 

If the function fails, use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.




## -remarks



The <b>dwForwardProto</b> member of 
<a href="https://msdn.microsoft.com/ff451481-3e9d-4add-94e2-846d67002a38">MIB_IPFORWARDROW</a> structure pointer to by the <i>route</i> parameter must be set to <b>MIB_IPPROTO_NETMGMT</b> otherwise <b>DeleteIpForwardEntry</b> will fail. Routing protocol identifiers are used to identify route information for the specified routing protocol. For example, <b>MIB_IPPROTO_NETMGMT</b> is used to identify route information for IP  routing set through network management such as the Dynamic Host Configuration Protocol (DHCP), the Simple Network Management Protocol (SNMP), or by calls to the <a href="https://msdn.microsoft.com/72243390-c3b8-41c3-8771-a5fb1d6383ae">CreateIpForwardEntry</a>,  <b>DeleteIpForwardEntry</b> 
		, or <a href="https://msdn.microsoft.com/a98de796-8fa2-4835-8d15-07d86d89c348">SetIpForwardEntry</a> functions.

On Windows Vista and Windows Server 2008, the <b>DeleteIpForwardEntry</b> only works on interfaces with a single sub-interface (where the interface LUID and subinterface LUID are the same). The <b>dwForwardIfIndex</b> member of the <a href="https://msdn.microsoft.com/ff451481-3e9d-4add-94e2-846d67002a38">MIB_IPFORWARDROW</a> structure specifies the interface.

A number of members of the <a href="https://msdn.microsoft.com/ff451481-3e9d-4add-94e2-846d67002a38">MIB_IPFORWARDROW</a> structure  pointed to by the <i>route</i> parameter are not currently used by <a href="https://msdn.microsoft.com/72243390-c3b8-41c3-8771-a5fb1d6383ae">CreateIpForwardEntry</a>. These members include <b>dwForwardPolicy</b>, <b>dwForwardType</b>, <b>dwForwardAge</b>, <b>dwForwardNextHopAS</b>, <b>dwForwardMetric1</b>, <b>dwForwardMetric2</b>, <b>dwForwardMetric3</b>, <b>dwForwardMetric4</b>, and <b>dwForwardMetric5</b>. 

To modify an existing route in the IPv4 routing table, use the 
<a href="https://msdn.microsoft.com/a98de796-8fa2-4835-8d15-07d86d89c348">SetIpForwardEntry</a> function. To retrieve the IPv4 routing table, call the <a href="https://msdn.microsoft.com/5d645353-7c87-4f8a-b7fd-149675a94743">GetIpForwardTable</a> function.

On Windows Vista and later, the <b>DeleteIpForwardEntry</b> function can only be called by a user logged on as a member of the Administrators group. If <b>DeleteIpForwardEntry</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. 

The <b>DeleteIpForwardEntry</b> function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.



<div class="alert"><b>Note</b>   On Windows NT 4.0 and Windows 2000 and later, this function executes a privileged operation. For this function to execute successfully, the caller must be logged on as a member of the Administrators group or the NetworkConfigurationOperators group.</div>
<div> </div>

#### Examples

The following code example shows how to change the default gateway to NewGateway. By calling GetIpForwardTable, changing the gateway, and then calling SetIpForwardEntry will not change the route, but will add a new one. If multiple default gateways exist, this code will delete them. Be aware that the new gateway must be viable; otherwise, TCP/IP will ignore the change.



<div class="alert"><b>Note</b>  Executing this code will change your IP routing tables and will likely cause network activity to fail.</div>
<div> </div>
<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include &lt;windows.h&gt;
#include &lt;winsock2.h&gt;
#include &lt;iphlpapi.h&gt;
#include &lt;stdio.h&gt;
#include &lt;stdlib.h&gt;

#pragma comment(lib, "iphlpapi.lib")

int main()
{
    // Declare and initialize variables
    PMIB_IPFORWARDTABLE pIpForwardTable = NULL;
    PMIB_IPFORWARDROW pRow = NULL;
    DWORD dwSize = 0;
    BOOL bOrder = FALSE;
    DWORD dwStatus = 0;
    DWORD NewGateway = 0xDDBBCCAA;      // this is in host order Ip Address AA.BB.CC.DD is DDCCBBAA

    unsigned int i;

// Identify the required size of the buffer.
    dwStatus = GetIpForwardTable(pIpForwardTable, &amp;dwSize, bOrder);
    if (dwStatus == ERROR_INSUFFICIENT_BUFFER) {
        // Allocate memory for the table.
        if (!(pIpForwardTable = (PMIB_IPFORWARDTABLE) malloc(dwSize))) {
            printf("Malloc failed. Out of memory.\n");
            exit(1);
        }
        // Retrieve the table.
        dwStatus = GetIpForwardTable(pIpForwardTable, &amp;dwSize, bOrder);
    }

    if (dwStatus != ERROR_SUCCESS) {
        printf("getIpForwardTable failed.\n");
        if (pIpForwardTable)
            free(pIpForwardTable);
        exit(1);
    }
// Search for the required row in the table. The default gateway has a destination
// of 0.0.0.0. Be aware the table continues to be searched, but only
// one row is copied. This is to ensure that, if multiple gateways exist, all of them are deleted.
// 
    for (i = 0; i &lt; pIpForwardTable-&gt;dwNumEntries; i++) {
        if (pIpForwardTable-&gt;table[i].dwForwardDest == 0) {
            // The default gateway was found.
            if (!pRow) {
                // Allocate memory to store the row. This is easier than manually filling
                // the row structure; only the gateway address is changed.
                //
                pRow = (PMIB_IPFORWARDROW) malloc(sizeof (MIB_IPFORWARDROW));
                if (!pRow) {
                    printf("Malloc failed. Out of memory.\n");
                    exit(1);
                }
                // Copy the row.
                memcpy(pRow, &amp;(pIpForwardTable-&gt;table[i]),
                       sizeof (MIB_IPFORWARDROW));
            }
            // Delete the old default gateway entry.
            dwStatus = DeleteIpForwardEntry(&amp;(pIpForwardTable-&gt;table[i]));

            if (dwStatus != ERROR_SUCCESS) {
                printf("Could not delete old gateway\n");
                exit(1);
            }
        }
    }

// Set the nexthop field to our new gateway. All other properties of the route will
// remain the same.
    pRow-&gt;dwForwardNextHop = NewGateway;

// Create a new route entry for the default gateway.
    dwStatus = CreateIpForwardEntry(pRow);

    if (dwStatus == NO_ERROR)
        printf("Gateway changed successfully\n");
    else if (dwStatus == ERROR_INVALID_PARAMETER)
        printf("Invalid parameter.\n");
    else
        printf("Error: %d\n", dwStatus);

// Free the memory. 
    if (pIpForwardTable)
        free(pIpForwardTable);
    if (pRow)
        free(pRow);

    exit(0);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/72243390-c3b8-41c3-8771-a5fb1d6383ae">CreateIpForwardEntry</a>



<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>



<a href="https://msdn.microsoft.com/5d645353-7c87-4f8a-b7fd-149675a94743">GetIpForwardTable</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/ff451481-3e9d-4add-94e2-846d67002a38">MIB_IPFORWARDROW</a>



<a href="https://msdn.microsoft.com/a98de796-8fa2-4835-8d15-07d86d89c348">SetIpForwardEntry</a>
 

 

