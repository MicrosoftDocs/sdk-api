---
UID: NF:iphlpapi.IpRenewAddress
title: IpRenewAddress function (iphlpapi.h)
description: The IpRenewAddressfunction renews a lease on an IPv4 address previously obtained through Dynamic Host Configuration Protocol (DHCP).
helpviewer_keywords: ["IpRenewAddress","IpRenewAddress function [IP Helper]","_iphlp_iprenewaddress","iphlp.iprenewaddress","iphlpapi/IpRenewAddress"]
old-location: iphlp\iprenewaddress.htm
tech.root: IpHlp
ms.assetid: 25b1bf9f-3ae1-453c-baae-5f70ae46cd24
ms.date: 12/05/2018
ms.keywords: IpRenewAddress, IpRenewAddress function [IP Helper], _iphlp_iprenewaddress, iphlp.iprenewaddress, iphlpapi/IpRenewAddress
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
 - IpRenewAddress
 - iphlpapi/IpRenewAddress
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
 - IpRenewAddress
---

# IpRenewAddress function


## -description

The 
<b>IpRenewAddress</b> function renews a lease on an IPv4 address previously obtained through Dynamic Host Configuration Protocol (DHCP).

## -parameters

### -param AdapterInfo [in]

A pointer to an 
<a href="/windows/desktop/api/ipexport/ns-ipexport-ip_adapter_index_map">IP_ADAPTER_INDEX_MAP</a> structure that specifies the adapter associated with the IP address to renew.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

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
An exception occurred during the request to DHCP for the renewal of the IPv4 address.

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

The 
<b>IpRenewAddress</b> function is specific to IPv4 and renews only an IPv4 address previously obtained through the Dynamic Host Configuration Protocol (DHCP). The <b>Name</b> member of the <a href="/windows/desktop/api/ipexport/ns-ipexport-ip_adapter_index_map">IP_ADAPTER_INDEX_MAP</a> structure pointed to by the <i>AdapterInfo</i> parameter is the only member used to determine the DHCP address to renew.

  An array of  <a href="/windows/desktop/api/ipexport/ns-ipexport-ip_adapter_index_map">IP_ADAPTER_INDEX_MAP</a> structures are returned in the <a href="/windows/desktop/api/ipexport/ns-ipexport-ip_interface_info">IP_INTERFACE_INFO</a> structure by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getinterfaceinfo">GetInterfaceInfo</a> function.  The <b>IP_INTERFACE_INFO</b> structure returned by <b>GetInterfaceInfo</b> contains at least one <b>IP_ADAPTER_INDEX_MAP</b> structure even if the <b>NumAdapters</b> member of the <b>IP_INTERFACE_INFO</b> structure indicates that no network adapters with IPv4 are enabled. When the <b>NumAdapters</b> member of the <b>IP_INTERFACE_INFO</b> structure returned by <b>GetInterfaceInfo</b> is zero, the value of the members of the single  <b>IP_ADAPTER_INDEX_MAP</b> structure returned in the <b>IP_INTERFACE_INFO</b> structure is undefined. 

If the <b>Name</b> member of the <a href="/windows/desktop/api/ipexport/ns-ipexport-ip_adapter_index_map">IP_ADAPTER_INDEX_MAP</a> structure pointed to by the <i>AdapterInfo</i> parameter is <b>NULL</b>, the 
<b>IpRenewAddress</b> function returns <b>ERROR_INVALID_PARAMETER</b>.

There are no functions available for releasing or renewing an IPv6 address. This can only be done by executing the Ipconfig command:
  

<b>ipconfig /release6
  </b>

<b>ipconfig /renew6</b>


#### Examples

The following example retrieves the list of network adapters with IPv4 enabled on the local system, then releases and renews the IPv4 address for the first adapter in the list.


```cpp
#include <windows.h>
#include <iphlpapi.h>
#include <stdio.h>

#pragma comment(lib, "iphlpapi.lib")

/* Note: could also use malloc() and free() */
#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x))
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))

void main()
{

    // Before calling IpReleaseAddress and IpRenewAddress we use
    // GetInterfaceInfo to retrieve a handle to the adapter

    PIP_INTERFACE_INFO pInfo;
    pInfo = (IP_INTERFACE_INFO *) MALLOC( sizeof(IP_INTERFACE_INFO) );
    ULONG ulOutBufLen = 0;
    DWORD dwRetVal = 0;

    // Make an initial call to GetInterfaceInfo to get
    // the necessary size into the ulOutBufLen variable
    if ( GetInterfaceInfo(pInfo, &ulOutBufLen) == ERROR_INSUFFICIENT_BUFFER) {
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
      FREE(pInfo);
      pInfo = NULL;
      return;
    }
    else {
      printf("GetInterfaceInfo failed.\n");
      LPVOID lpMsgBuf;
                
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
      printf("IP release failed.\n");
    }

    if ((dwRetVal = IpRenewAddress(&pInfo->Adapter[0])) == NO_ERROR) {
      printf("IP renew succeeded.\n");
    }
    else {
      printf("IP renew failed.\n");
    }

    /* Free allocated memory no longer needed */
    if (pInfo) {
        FREE(pInfo);
        pInfo = NULL;
    }
}


```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getinterfaceinfo">GetInterfaceInfo</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-ip_adapter_index_map">IP_ADAPTER_INDEX_MAP</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-ip_interface_info">IP_INTERFACE_INFO</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-ipreleaseaddress">IpReleaseAddress</a>