---
UID: NF:iphlpapi.DeleteIPAddress
title: DeleteIPAddress function (iphlpapi.h)
description: The DeleteIPAddress function deletes an IP address previously added using AddIPAddress.
helpviewer_keywords: ["DeleteIPAddress","DeleteIPAddress function [IP Helper]","_iphlp_deleteipaddress","iphlp.deleteipaddress","iphlpapi/DeleteIPAddress"]
old-location: iphlp\deleteipaddress.htm
tech.root: IpHlp
ms.assetid: d7ed986d-d62e-4723-ab74-85c3edfdf4ff
ms.date: 12/05/2018
ms.keywords: DeleteIPAddress, DeleteIPAddress function [IP Helper], _iphlp_deleteipaddress, iphlp.deleteipaddress, iphlpapi/DeleteIPAddress
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
 - DeleteIPAddress
 - iphlpapi/DeleteIPAddress
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
 - DeleteIPAddress
---

# DeleteIPAddress function


## -description

The 
<b>DeleteIPAddress</b> function deletes an IP address previously added using 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-addipaddress">AddIPAddress</a>.

## -parameters

### -param NTEContext [in]

The Net Table Entry (NTE) context for the IP address. This context was returned by the previous call to 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-addipaddress">AddIPAddress</a>.

## -returns

The function returns <b>NO_ERROR</b> (zero) if the function is successful. 

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An input parameter is invalid, no action was taken.  

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

On Windows Vista and later, the <b>DeleteIPAddress</b> function can only be called by a user logged on as a member of the Administrators group. If <b>DeleteIPAddress</b> is called by a user that is not a member of the Administrators group, the function call will fail and <b>ERROR_ACCESS_DENIED</b> is returned. This function can also fail because of user account control (UAC) on Windows Vista and later. If an application that contains this function is executed by a user logged on as a member of the Administrators group other than the built-in Administrator, this call will fail unless the application has been marked in the manifest file with a <b>requestedExecutionLevel</b> set to requireAdministrator. If the application on Windows Vista and later lacks this manifest file, a user logged on as a member of the Administrators group other than the built-in Administrator must then be executing the application in an enhanced shell as the built-in Administrator (RunAs administrator) for this function to succeed.



<div class="alert"><b>Note</b>  On Windows NT 4.0 and Windows 2000 and later, this function executes a privileged operation. For this function to execute successfully, the caller must be logged on as a member of the Administrators group or the NetworkConfigurationOperators group.</div>
<div> </div>

#### Examples

The following example retrieves the IP address table, then adds the IP address 192.168.0.27 to the first adapter. The IP address that was added is then deleted.


```cpp
#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <iphlpapi.h>
#include <stdio.h>
#include <stdlib.h>

#pragma comment(lib, "iphlpapi.lib")
#pragma comment(lib, "ws2_32.lib")

int main()
{
    // Declare and initialize variables
    PMIB_IPADDRTABLE pIPAddrTable;
    DWORD dwSize = 0;
    DWORD dwRetVal;

    // IP and mask we will be adding
    UINT iaIPAddress;
    UINT imIPMask;

    // Variables where handles to the added IP will be returned
    ULONG NTEContext = 0;
    ULONG NTEInstance = 0;

    LPVOID lpMsgBuf;


    // Before calling AddIPAddress we use GetIpAddrTable to get
    // an adapter to which we can add the IP.
    pIPAddrTable = (MIB_IPADDRTABLE *) malloc(sizeof (MIB_IPADDRTABLE));

    // Make an initial call to GetIpAddrTable to get the
    // necessary size into the dwSize variable
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        GlobalFree(pIPAddrTable);
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc(dwSize);
    }
    // Make a second call to GetIpAddrTable to get the
    // actual data we want
    if ((dwRetVal = GetIpAddrTable(pIPAddrTable, &dwSize, 0)) == NO_ERROR) {
        printf("\tAddress: %ld\n", pIPAddrTable->table[0].dwAddr);
        printf("\tMask:    %ld\n", pIPAddrTable->table[0].dwMask);
        printf("\tIndex:   %ld\n", pIPAddrTable->table[0].dwIndex);
        printf("\tBCast:   %ld\n", pIPAddrTable->table[0].dwBCastAddr);
        printf("\tReasm:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    } else {
        printf("Call to GetIpAddrTable failed.\n");
    }

    // IP and mask we will be adding

    iaIPAddress = inet_addr("192.168.0.27");
    imIPMask = inet_addr("255.255.255.0");

    if ((dwRetVal = AddIPAddress(iaIPAddress,
                                 imIPMask,
                                 pIPAddrTable->table[0].dwIndex,
                                 &NTEContext, &NTEInstance)) == NO_ERROR) {
        printf("\tIP address added.\n");
    }

    else {
        printf("Error adding IP address.\n");

        if (FormatMessage(FORMAT_MESSAGE_ALLOCATE_BUFFER | FORMAT_MESSAGE_FROM_SYSTEM | FORMAT_MESSAGE_IGNORE_INSERTS, NULL, dwRetVal, MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT),       // Default language
                          (LPTSTR) & lpMsgBuf, 0, NULL)) {
            printf("\tError: %s", lpMsgBuf);
        }
        LocalFree(lpMsgBuf);
    }

    // Delete the IP we just added using the NTEContext
    // variable where the handle was returned       
    if ((dwRetVal = DeleteIPAddress(NTEContext)) == NO_ERROR) {
        printf("\tIP Address Deleted.\n");
    } else {
        printf("\tCall to DeleteIPAddress failed.\n");
    }

    exit(0);

```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-addipaddress">AddIPAddress</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>