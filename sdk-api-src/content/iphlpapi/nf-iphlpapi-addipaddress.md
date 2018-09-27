---
UID: NF:iphlpapi.AddIPAddress
title: AddIPAddress function
author: windows-sdk-content
description: The AddIPAddress function adds the specified IPv4 address to the specified adapter.
old-location: iphlp\addipaddress.htm
tech.root: IpHlp
ms.assetid: 669264cd-a43c-4681-9416-2704d4232685
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AddIPAddress, AddIPAddress function [IP Helper], _iphlp_addipaddress, iphlp.addipaddress, iphlpapi/AddIPAddress
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
 - AddIPAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AddIPAddress function


## -description


The 
<b>AddIPAddress</b> function adds the specified IPv4 address to the specified adapter.


## -parameters




### -param Address [in]

The IPv4 address to add to the adapter, in the form of an <a href="https://msdn.microsoft.com/00d4823d-114d-4cc7-afdf-54c7fed3fe45">IPAddr</a> structure.


### -param IpMask [in]

The subnet mask for the IPv4 address specified in the <i>Address</i> parameter.   The <b>IPMask</b> parameter uses the same format as an <a href="https://msdn.microsoft.com/00d4823d-114d-4cc7-afdf-54c7fed3fe45">IPAddr</a> structure.


### -param IfIndex [in]

The index of the adapter on which to add the IPv4 address.


### -param NTEContext [out]

A pointer to a <b>ULONG</b> variable. On successful return, this parameter points to the Net Table Entry (NTE) context for the IPv4 address that was added. The caller can later use this context in a call to 
the <a href="https://msdn.microsoft.com/d7ed986d-d62e-4723-ab74-85c3edfdf4ff">DeleteIPAddress</a> function.


### -param NTEInstance [out]

A pointer to a <b>ULONG</b> variable. On successful return, this parameter points to the NTE instance for the IPv4 address that was added.


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
<dt><b>ERROR_DEV_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The adapter specified by the <i>IfIndex</i> parameter does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DUP_DOMAINNAME</b></dt>
</dl>
</td>
<td width="60%">
The IPv4 address to add that is specified in the <i>Address</i> parameter already exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_GEN_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
A general failure. This error is returned for some values specified in the <i>Address</i> parameter, such as an IPv4 address normally considered to be a broadcast addresses.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The user attempting to make the function call is not an administrator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters is invalid. This error is returned if the <i>NTEContext</i> or <i>NTEInstance</i> parameters are <b>NULL</b>. This error is also returned when the IP address specified in the <i>Address</i> parameter is inconsistent with the interface index specified in the <i>IfIndex</i> parameter (for example, a loopback address on a non-loopback interface).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The function call is not supported on the version of Windows on which it was run.

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



The <b>AddIPAddress</b> function is used to add a new IPv4 address entry on a local computer. The IPv4 address added by 
the <b>AddIPAddress</b> function is not persistent. The IPv4 address exists only as long as the adapter object exists. Restarting the computer destroys the IPv4 address, as does manually resetting the network interface card (NIC). Also, certain PnP events may destroy the address.

To create an IPv4 address that persists, the <a href="https://msdn.microsoft.com/d0076424-58c0-4cfe-b55b-44c0f2620388">EnableStatic method of the Win32_NetworkAdapterConfiguration Class</a> in the Windows Management Instrumentation (WMI) controls may be used. The netsh commands can also be used to create a persistent IPv4 address. 

For more information, please see the documentation on <a href="https://msdn.microsoft.com/68e17a55-4dd5-40cd-8996-25fa278ddd19">Netsh.exe</a> in the Windows Sockets documentation.

On  Windows Server 2003, Windows XP, and Windows 2000, if the IPv4 address in the <i>Address</i> parameter already exists on the network, the <b>AddIPAddress</b> function returns <b>NO_ERROR</b> and  the IPv4 address added is 0.0.0.0. 

On  Windows Vista and later, if the IPv4 address passed in the <i>Address</i> parameter already exists on the network, the <b>AddIPAddress</b> function returns <b>NO_ERROR</b> and  the duplicate IPv4 address is added with the <b>IP_DAD_STATE</b> member in  the <a href="https://msdn.microsoft.com/65c3648c-89bd-417b-8a9b-feefa6149c4a">IP_ADAPTER_UNICAST_ADDRESS</a> structure set to <b>IpDadStateDuplicate</b>. 

An IPv4 address that is added using the <b>AddIPAddress</b> function can later be deleted by calling the <a href="https://msdn.microsoft.com/d7ed986d-d62e-4723-ab74-85c3edfdf4ff">DeleteIPAddress</a> function  passing the  <i>NTEContext</i> parameter returned by the <b>AddIPAddress</b> function.

For information about the <b>IPAddr</b> and <b>IPMask</b> data types, see 
<a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">Windows Data Types</a>. To convert an IPv4 address between dotted decimal notation and <b>IPAddr</b> format, use the 
<a href="https://msdn.microsoft.com/7d6df658-9d83-45c7-97e7-b2a016a73847">inet_addr</a> and 
<a href="https://msdn.microsoft.com/01cd32e7-a01d-40e8-afb5-69223d643a0e">inet_ntoa</a> functions.

On Windows Vista and later, the <a href="https://msdn.microsoft.com/8afca4e9-a4c4-4f93-bb4d-25e2eea71ae0">CreateUnicastIpAddressEntry</a> function can be used to add a new unicast IPv4 or IPv6 address entry on a local computer. 


#### Examples

The following example retrieves the IP address table to determine the interface index for the first adapter, then adds the IP address specified on command line to the first adapter. The IP address that was added is then deleted.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#pragma comment(lib, "iphlpapi.lib")
#pragma comment(lib, "ws2_32.lib")

#include &lt;winsock2.h&gt;
#include &lt;ws2tcpip.h&gt;
#include &lt;iphlpapi.h&gt;
#include &lt;stdio.h&gt;

#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x))
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))

/* Note: could also use malloc() and free() */

int __cdecl main(int argc, char **argv)
{

    /* Variables used by GetIpAddrTable */
    PMIB_IPADDRTABLE pIPAddrTable;
    DWORD dwSize = 0;
    DWORD dwRetVal = 0;
    IN_ADDR IPAddr;
    DWORD ifIndex;

    /* IPv4 address and subnet mask we will be adding */
    UINT iaIPAddress;
    UINT iaIPMask;

    /* Variables where handles to the added IP are returned */
    ULONG NTEContext = 0;
    ULONG NTEInstance = 0;

    /* Variables used to return error message */
    LPVOID lpMsgBuf;

    // Validate the parameters
    if (argc != 3) {
        printf("usage: %s IPAddress SubnetMask\n", argv[0]);
        exit(1);
    }

    iaIPAddress = inet_addr(argv[1]);
    if (iaIPAddress == INADDR_NONE) {
        printf("usage: %s IPAddress SubnetMask\n", argv[0]);
        exit(1);
    }

    iaIPMask = inet_addr(argv[2]);
    if (iaIPMask == INADDR_NONE) {
        printf("usage: %s IPAddress SubnetMask\n", argv[0]);
        exit(1);
    }

    // Before calling AddIPAddress we use GetIpAddrTable to get
    // an adapter to which we can add the IP.
    pIPAddrTable = (MIB_IPADDRTABLE *) MALLOC(sizeof (MIB_IPADDRTABLE));
    if (pIPAddrTable == NULL) {
        printf("Error allocating memory needed to call GetIpAddrTable\n");
        exit (1);
    }
    else {
        dwSize = 0;
        // Make an initial call to GetIpAddrTable to get the
        // necessary size into the dwSize variable
        if (GetIpAddrTable(pIPAddrTable, &amp;dwSize, 0) ==
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
    if ((dwRetVal = GetIpAddrTable(pIPAddrTable, &amp;dwSize, 0)) == NO_ERROR) {
        // Save the interface index to use for adding an IP address
        ifIndex = pIPAddrTable-&gt;table[0].dwIndex;
        printf("\n\tInterface Index:\t%ld\n", ifIndex);
        IPAddr.S_un.S_addr = (u_long) pIPAddrTable-&gt;table[0].dwAddr;
        printf("\tIP Address:       \t%s (%lu%)\n", inet_ntoa(IPAddr),
               pIPAddrTable-&gt;table[0].dwAddr);
        IPAddr.S_un.S_addr = (u_long) pIPAddrTable-&gt;table[0].dwMask;
        printf("\tSubnet Mask:      \t%s (%lu%)\n", inet_ntoa(IPAddr),
               pIPAddrTable-&gt;table[0].dwMask);
        IPAddr.S_un.S_addr = (u_long) pIPAddrTable-&gt;table[0].dwBCastAddr;
        printf("\tBroadCast Address:\t%s (%lu%)\n", inet_ntoa(IPAddr),
               pIPAddrTable-&gt;table[0].dwBCastAddr);
        printf("\tReassembly size:  \t%lu\n\n",
               pIPAddrTable-&gt;table[0].dwReasmSize);
    } else {
        printf("Call to GetIpAddrTable failed with error %d.\n", dwRetVal);
        if (pIPAddrTable)
            FREE(pIPAddrTable);
        exit(1);
    }

    if (pIPAddrTable) {
        FREE(pIPAddrTable);
        pIPAddrTable = NULL;
    }

    if ((dwRetVal = AddIPAddress(iaIPAddress,
                                 iaIPMask,
                                 ifIndex,
                                 &amp;NTEContext, &amp;NTEInstance)) == NO_ERROR) {
        printf("\tIPv4 address %s was successfully added.\n", argv[1]);
    } else {
        printf("AddIPAddress failed with error: %d\n", dwRetVal);

        if (FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM | FORMAT_MESSAGE_IGNORE_INSERTS, NULL, dwRetVal, MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),       // Default language
                          (LPTSTR) &amp; lpMsgBuf, 0, NULL)) {
            printf("\tError: %s", lpMsgBuf);
            LocalFree(lpMsgBuf);
            exit(1);
        }
    }

// Delete the IP we just added using the NTEContext
// variable where the handle was returned       
    if ((dwRetVal = DeleteIPAddress(NTEContext)) == NO_ERROR) {
        printf("\tIPv4 address %s was successfully deleted.\n", argv[1]);
    } else {
        printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
        exit(1);
    }

    exit(0);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8afca4e9-a4c4-4f93-bb4d-25e2eea71ae0">CreateUnicastIpAddressEntry</a>



<a href="https://msdn.microsoft.com/d7ed986d-d62e-4723-ab74-85c3edfdf4ff">DeleteIPAddress</a>



<a href="https://msdn.microsoft.com/e98ee6b3-30c2-4629-859e-e7440781cd86">GetAdapterIndex</a>



<a href="https://msdn.microsoft.com/03bf5645-8237-4c78-a921-47315cab1c44">GetIpAddrTable</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/00d4823d-114d-4cc7-afdf-54c7fed3fe45">IPAddr</a>
 

 

