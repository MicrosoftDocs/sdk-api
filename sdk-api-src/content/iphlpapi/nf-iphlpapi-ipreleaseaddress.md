---
UID: NF:iphlpapi.IpReleaseAddress
title: IpReleaseAddress function
author: windows-sdk-content
description: The IpReleaseAddress function releases an IPv4 address previously obtained through the Dynamic Host Configuration Protocol (DHCP).
old-location: iphlp\ipreleaseaddress.htm
tech.root: iphlp
ms.assetid: d937ea44-1ca3-49e0-913d-fb77888d05fc
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: IpReleaseAddress, IpReleaseAddress function [IP Helper], _iphlp_ipreleaseaddress, iphlp.ipreleaseaddress, iphlpapi/IpReleaseAddress
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
 - IpReleaseAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IpReleaseAddress function


## -description


The 
<b>IpReleaseAddress</b> function releases an IPv4 address previously obtained through the Dynamic Host Configuration Protocol (DHCP).


## -parameters




### -param AdapterInfo [in]

A pointer to an 
<a href="https://msdn.microsoft.com/83d95ef3-13a4-4124-84cd-3016e9fb4446">IP_ADAPTER_INDEX_MAP</a> structure that specifies the adapter associated with the IPv4 address to release.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, use 
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

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
One of the parameters is invalid. This error is returned if the <i>AdapterInfo</i> parameter is <b>NULL</b> or if the <b>Name</b> member of the <b>PIP_ADAPTER_INDEX_MAP</b> structure pointed to by the <i>AdapterInfo</i> parameter is invalid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PROC_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred during the request to DHCP for the release of the IPv4 address.

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



The 
<b>IpReleaseAddress</b> function is specific to IPv4 and releases only an IPv4 address previously obtained through the Dynamic Host Configuration Protocol (DHCP). The <b>Name</b> member of the <a href="https://msdn.microsoft.com/83d95ef3-13a4-4124-84cd-3016e9fb4446">IP_ADAPTER_INDEX_MAP</a> structure pointed to by the <i>AdapterInfo</i> parameter is the only member used to determine the DHCP address to release. 

An array of <a href="https://msdn.microsoft.com/83d95ef3-13a4-4124-84cd-3016e9fb4446">IP_ADAPTER_INDEX_MAP</a> structures is returned in the <a href="https://msdn.microsoft.com/287a4574-0a0f-4f20-932b-22bb6f40401d">IP_INTERFACE_INFO</a> structure by the <a href="https://msdn.microsoft.com/efc0d175-2c6d-4608-b385-1623a9e0375c">GetInterfaceInfo</a> function.  The <b>IP_INTERFACE_INFO</b> structure returned by <b>GetInterfaceInfo</b> contains at least one <b>IP_ADAPTER_INDEX_MAP</b> structure even if the <b>NumAdapters</b> member of the <b>IP_INTERFACE_INFO</b> structure indicates that no network adapters with IPv4 are enabled. When the <b>NumAdapters</b> member of the <b>IP_INTERFACE_INFO</b> structure returned by <b>GetInterfaceInfo</b> is zero, the value of the members of the single  <b>IP_ADAPTER_INDEX_MAP</b> structure returned in the <b>IP_INTERFACE_INFO</b> structure is undefined. 

If the <b>Name</b> member of the <a href="https://msdn.microsoft.com/83d95ef3-13a4-4124-84cd-3016e9fb4446">IP_ADAPTER_INDEX_MAP</a> structure pointed to by the <i>AdapterInfo</i> parameter is <b>NULL</b>, the 
<b>IpReleaseAddress</b> function returns <b>ERROR_INVALID_PARAMETER</b>.  

There are no functions available for releasing or renewing an IPv6 address. This can only be done by executing the Ipconfig command:
  

<b>ipconfig /release6
  </b>

<b>ipconfig /renew6</b>


#### Examples

The following example retrieves the list of network adapters with IPv4 enabled on the local system, then releases and renews the IPv4 address for the first adapter in the list.


```cpp
#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <winsock2.h>
#include <iphlpapi.h>
#include <stdio.h>

#pragma comment(lib, "iphlpapi.lib")

#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x)) 
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))

// Before calling IpReleaseAddress and IpRenewAddress we use
// GetInterfaceInfo to retrieve a handle to the adapter

void __cdecl main()
{
    ULONG ulOutBufLen = 0;
    DWORD dwRetVal = 0;
    PIP_INTERFACE_INFO pInfo;

    pInfo = (IP_INTERFACE_INFO *) MALLOC(sizeof(IP_INTERFACE_INFO));

    // Make an initial call to GetInterfaceInfo to get
    // the necessary size into the ulOutBufLen variable
    if (GetInterfaceInfo(pInfo, &ulOutBufLen) == ERROR_INSUFFICIENT_BUFFER) {
        FREE(pInfo);
        pInfo = (IP_INTERFACE_INFO *) MALLOC (ulOutBufLen);
    }

    // Make a second call to GetInterfaceInfo to get the
    // actual data we want
    if ((dwRetVal = GetInterfaceInfo(pInfo, &ulOutBufLen)) == NO_ERROR ) {
        printf("\tAdapter Name: %ws\n", pInfo->Adapter[0].Name);
        printf("\tAdapter Index: %ld\n", pInfo->Adapter[0].Index);
        printf("\tNum Adapters: %ld\n", pInfo->NumAdapters);
    }
    else if (dwRetVal == ERROR_NO_DATA) {
        printf("There are no network adapters with IPv4 enabled on the local system\n");
        return;
    }
    else {
        LPVOID lpMsgBuf;
        printf("GetInterfaceInfo failed.\n");
            
        if (FormatMessage( 
            FORMAT_MESSAGE_ALLOCATE_BUFFER | 
            FORMAT_MESSAGE_FROM_SYSTEM | 
            FORMAT_MESSAGE_IGNORE_INSERTS,
            NULL,
            dwRetVal,
            MAKELANGID(LANG_NEUTRAL, SUBLANG_DEFAULT), // Default language
            (LPTSTR) &lpMsgBuf,
            0,
            NULL )) {
            printf("\tError: %s", lpMsgBuf);
        }
        LocalFree( lpMsgBuf );
        return;
    }

// Call IpReleaseAddress and IpRenewAddress to release and renew
// the IP address on the first network adapter returned 
// by the call to GetInterfaceInfo.
    if ((dwRetVal = IpReleaseAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("IP release succeeded.\n");
    }
    else {
        printf("IP release failed: %ld\n", dwRetVal);
    }

    if ((dwRetVal = IpRenewAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("IP renew succeeded.\n");
    }
    else {
        printf("IP renew failed: %ld\n", dwRetVal);
    }

    // Free memory for IP_INTERFACE_INFO 
    if (pInfo != NULL) {
        FREE(pInfo);
    }
    return;
}

```





## -see-also




<a href="https://msdn.microsoft.com/efc0d175-2c6d-4608-b385-1623a9e0375c">GetInterfaceInfo</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/83d95ef3-13a4-4124-84cd-3016e9fb4446">IP_ADAPTER_INDEX_MAP</a>



<a href="https://msdn.microsoft.com/287a4574-0a0f-4f20-932b-22bb6f40401d">IP_INTERFACE_INFO</a>



<a href="https://msdn.microsoft.com/25b1bf9f-3ae1-453c-baae-5f70ae46cd24">IpRenewAddress</a>
 

 

