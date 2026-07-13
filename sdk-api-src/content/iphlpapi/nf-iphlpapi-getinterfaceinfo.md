---
UID: NF:iphlpapi.GetInterfaceInfo
title: GetInterfaceInfo function (iphlpapi.h)
description: The GetInterfaceInfo function obtains the list of the network interface adapters with IPv4 enabled on the local system.
helpviewer_keywords: ["GetInterfaceInfo","GetInterfaceInfo function [IP Helper]","_iphlp_getinterfaceinfo","iphlp.getinterfaceinfo","iphlpapi/GetInterfaceInfo"]
old-location: iphlp\getinterfaceinfo.htm
tech.root: IpHlp
ms.assetid: efc0d175-2c6d-4608-b385-1623a9e0375c
ms.date: 12/05/2018
ms.keywords: GetInterfaceInfo, GetInterfaceInfo function [IP Helper], _iphlp_getinterfaceinfo, iphlp.getinterfaceinfo, iphlpapi/GetInterfaceInfo
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
 - GetInterfaceInfo
 - iphlpapi/GetInterfaceInfo
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
 - GetInterfaceInfo
---

# GetInterfaceInfo function


## -description

The 
<b>GetInterfaceInfo</b> function obtains the list of the network interface adapters with IPv4 enabled on the local system.

## -parameters

### -param pIfTable [out]

A pointer to a buffer that specifies an 
<a href="/windows/desktop/api/ipexport/ns-ipexport-ip_interface_info">IP_INTERFACE_INFO</a> structure that receives the list of adapters. This buffer must be allocated by the caller.

### -param dwOutBufLen [in, out]

A pointer to a <b>DWORD</b> variable that specifies the size of the 
buffer pointed to by <i>pIfTable</i> parameter to receive the <a href="/windows/desktop/api/ipexport/ns-ipexport-ip_interface_info">IP_INTERFACE_INFO</a> structure. If this size is insufficient to hold the IPv4 interface information, 
<b>GetInterfaceInfo</b> fills in this variable with the required size, and returns an error code of <b>ERROR_INSUFFICIENT_BUFFER</b>.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer to receive the IPv4 adapter information is too small. This value is returned if the  <i>dwOutBufLen</i> parameter indicates that the buffer pointed to by the <i>pIfTable</i> parameter is too small to retrieve the IPv4 interface information. The required size is returned in the <b>DWORD</b> variable pointed to by the <i>dwOutBufLen</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if the <i>dwOutBufLen</i> parameter is <b>NULL</b>, or <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getinterfaceinfo">GetInterfaceInfo</a> is unable to write to the memory pointed to by the <i>dwOutBufLen</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_DATA</b></dt>
</dl>
</td>
<td width="60%">
There are no network adapters enabled for IPv4 on the local system. This value is also returned if all network adapters on the local system are disabled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This function is not supported on the operating system in use on the local system.

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
<b>GetInterfaceInfo</b> function is specific to network adapters with IPv4 enabled. The function returns an <a href="/windows/desktop/api/ipexport/ns-ipexport-ip_interface_info">IP_INTERFACE_INFO</a> structure pointed to by the <i>pIfTable</i> parameter that contains the number of network adapters with IPv4 enabled on the local system and an array of <a href="/windows/desktop/api/ipexport/ns-ipexport-ip_adapter_index_map">IP_ADAPTER_INDEX_MAP</a> structures with information on each network adapter with IPv4 enabled. The <b>IP_INTERFACE_INFO</b> structure returned by <b>GetInterfaceInfo</b> contains at least one <b>IP_ADAPTER_INDEX_MAP</b> structure even if the <b>NumAdapters</b> member of the <b>IP_INTERFACE_INFO</b> structure indicates that no network adapters with IPv4 are enabled. When the <b>NumAdapters</b> member of the <b>IP_INTERFACE_INFO</b> structure returned by <b>GetInterfaceInfo</b> is zero, the value of the members of the single  <b>IP_ADAPTER_INDEX_MAP</b> structure returned in the <b>IP_INTERFACE_INFO</b> structure is undefined. 

If the  <b>GetInterfaceInfo</b> function is called with too small a buffer to retrieve the IPv4 interface information  (the  <i>dwOutBufLen</i> parameter indicates that the buffer pointed to by the <i>pIfTable</i> parameter is too small), the function returns  <b>ERROR_INSUFFICIENT_BUFFER</b>. The required size is returned in the <b>DWORD</b> variable pointed to by the <i>dwOutBufLen</i> parameter.

 The  correct way to use the <b>GetInterfaceInfo</b> function is to call this function twice. In the first call, pass a <b>NULL</b> pointer in the <i>pIfTable</i> parameter and zero in the variable pointed to by the <i>dwOutBufLen</i> parameter. The call will fail with <b>ERROR_INSUFFICIENT_BUFFER</b> and the required size for this buffer is returned in the <b>DWORD</b> variable pointed to by the <i>dwOutBufLen</i> parameter. A buffer can then  be allocated of the required size using the value pointed by the <i>dwOutBufLen</i>. Then  the <b>GetInterfaceInfo</b> function can be called a second time with a pointer to this buffer passed in the <i>pIfTable</i> parameter and the length of the buffer set to the size of this buffer. 

The 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersinfo">GetAdaptersInfo</a> and 
<b>GetInterfaceInfo</b> functions do not return information about the loopback interface. Information on the loopback interface is returned by the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipaddrtable">GetIpAddrTable</a> function.

On Windows Vista and later, the <b>Name</b> member of the <a href="/windows/desktop/api/ipexport/ns-ipexport-ip_adapter_index_map">IP_ADAPTER_INDEX_MAP</a> structure returned in the <a href="/windows/desktop/api/ipexport/ns-ipexport-ip_interface_info">IP_INTERFACE_INFO</a> structure may be a Unicode string of the GUID for the network interface (the string begins with the '{' character). 


#### Examples

The following example retrieves the list of network adapters with IPv4 enabled on the local system and prints various properties of the first network adapter.


```cpp
#include <winsock2.h>
#include <ws2ipdef.h>
#include <iphlpapi.h>
#include <stdio.h>

#pragma comment(lib, "iphlpapi.lib")

#define MALLOC(x) HeapAlloc(GetProcessHeap(), 0, (x)) 
#define FREE(x) HeapFree(GetProcessHeap(), 0, (x))

/* Note: could also use malloc() and free() */

int main()
{

// Declare and initialize variables
    PIP_INTERFACE_INFO pInfo = NULL;
    ULONG ulOutBufLen = 0;

    DWORD dwRetVal = 0;
    int iReturn = 1;

    int i;

// Make an initial call to GetInterfaceInfo to get
// the necessary size in the ulOutBufLen variable
    dwRetVal = GetInterfaceInfo(NULL, &ulOutBufLen);
    if (dwRetVal == ERROR_INSUFFICIENT_BUFFER) {
        pInfo = (IP_INTERFACE_INFO *) MALLOC(ulOutBufLen);
        if (pInfo == NULL) {
            printf
                ("Unable to allocate memory needed to call GetInterfaceInfo\n");
            return 1;
        }
    }
// Make a second call to GetInterfaceInfo to get
// the actual data we need
    dwRetVal = GetInterfaceInfo(pInfo, &ulOutBufLen);
    if (dwRetVal == NO_ERROR) {
        printf("Number of Adapters: %ld\n\n", pInfo->NumAdapters);
        for (i = 0; i < pInfo->NumAdapters; i++) {
            printf("Adapter Index[%d]: %ld\n", i,
                   pInfo->Adapter[i].Index);
            printf("Adapter Name[%d]: %ws\n\n", i,
                   pInfo->Adapter[i].Name);
        }
        iReturn = 0;
    } else if (dwRetVal == ERROR_NO_DATA) {
        printf
            ("There are no network adapters with IPv4 enabled on the local system\n");
        iReturn = 0;
    } else {
        printf("GetInterfaceInfo failed with error: %d\n", dwRetVal);
        iReturn = 1;
    }

    FREE(pInfo);
    return (iReturn);
}


```

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersinfo">GetAdaptersInfo</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getipaddrtable">GetIpAddrTable</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getnumberofinterfaces">GetNumberOfInterfaces</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-ip_adapter_index_map">IP_ADAPTER_INDEX_MAP</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-ip_interface_info">IP_INTERFACE_INFO</a>
