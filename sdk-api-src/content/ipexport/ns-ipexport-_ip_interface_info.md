---
UID: NS:ipexport._IP_INTERFACE_INFO
title: "_IP_INTERFACE_INFO"
author: windows-sdk-content
description: The IP_INTERFACE_INFO structure contains a list of the network interface adapters with IPv4 enabled on the local system.
old-location: iphlp\ip_interface_info.htm
old-project: IpHlp
ms.assetid: 287a4574-0a0f-4f20-932b-22bb6f40401d
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PIP_INTERFACE_INFO, IP_INTERFACE_INFO, IP_INTERFACE_INFO structure [IP Helper], PIP_INTERFACE_INFO, PIP_INTERFACE_INFO structure pointer [IP Helper], _IP_INTERFACE_INFO, _iphlp_ip_interface_info, ipexport/IP_INTERFACE_INFO, ipexport/PIP_INTERFACE_INFO, iphlp.ip_interface_info"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ipexport.h
req.include-header: Iphlpapi.h
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
tech.root: 
req.typenames: IP_INTERFACE_INFO, *PIP_INTERFACE_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipexport.h
api_name:
 - IP_INTERFACE_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _IP_INTERFACE_INFO structure


## -description



			The 
<b>IP_INTERFACE_INFO</b> structure contains a list of the network interface adapters with IPv4 enabled on the local system.


## -struct-fields




### -field NumAdapters

The number of adapters listed in the array pointed to by the <b>Adapter</b> member.


### -field Adapter

An array of 
<a href="https://msdn.microsoft.com/83d95ef3-13a4-4124-84cd-3016e9fb4446">IP_ADAPTER_INDEX_MAP</a> structures. Each structure maps an adapter index to that adapter's name.  The adapter index  may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.


## -remarks



The 
<b>IP_INTERFACE_INFO</b> structure is specific to network adapters with IPv4 enabled. The <b>IP_INTERFACE_INFO</b> structure contains the number of network adapters with IPv4 enabled on the local system and an array of <a href="https://msdn.microsoft.com/83d95ef3-13a4-4124-84cd-3016e9fb4446">IP_ADAPTER_INDEX_MAP</a> structures with information on each network adapter with IPv4 enabled. The <b>IP_INTERFACE_INFO</b> structure contains at least one <b>IP_ADAPTER_INDEX_MAP</b> structure even if the <b>NumAdapters</b> member of the <b>IP_INTERFACE_INFO</b> structure indicates that no network adapters with IPv4 are enabled. When the <b>NumAdapters</b> member of the <b>IP_INTERFACE_INFO</b> structure is zero, the value of the members of the single  <b>IP_ADAPTER_INDEX_MAP</b> structure returned in the <b>IP_INTERFACE_INFO</b> structure is undefined. 

The 
<b>IP_INTERFACE_INFO</b> structure can't be used to return information about the loopback interface.

On Windows Vista and later, the <b>Name</b> member of the <a href="https://msdn.microsoft.com/83d95ef3-13a4-4124-84cd-3016e9fb4446">IP_ADAPTER_INDEX_MAP</a> structure in the <b>IP_INTERFACE_INFO</b> structure may be a Unicode string of the GUID for the network interface (the string begins with the '{' character). 

This structure is defined in the <i>Ipexport.h</i> header file which is automatically included in the <i>Iphlpapi.h</i> header file. The <i>Ipexport.h</i> header file should never be used directly.




#### Examples

The following example retrieves the list of network adapters with IPv4 enabled on the local system and prints various properties of the first adapter.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Declare and initialize variables
PIP_INTERFACE_INFO pInfo;
pInfo = (IP_INTERFACE_INFO *) malloc( sizeof(IP_INTERFACE_INFO) );
ULONG ulOutBufLen = 0;
DWORD dwRetVal = 0;


// Make an initial call to GetInterfaceInfo to get
// the necessary size in the ulOutBufLen variable
if ( GetInterfaceInfo(pInfo, &amp;ulOutBufLen) == ERROR_INSUFFICIENT_BUFFER) {
  free(pInfo);
  pInfo = (IP_INTERFACE_INFO *) malloc (ulOutBufLen);
}

// Make a second call to GetInterfaceInfo to get
// the actual data we need
if ((dwRetVal = GetInterfaceInfo(pInfo, &amp;ulOutBufLen)) == NO_ERROR ) {
  printf("\tAdapter Name: %ws\n", pInfo-&gt;Adapter[0].Name);
  printf("\tAdapter Index: %ld\n", pInfo-&gt;Adapter[0].Index);
  printf("\tNum Adapters: %ld\n", pInfo-&gt;NumAdapters);

  // free memory allocated
  free(pInfo);
  pInfo = NULL;
}  
else if (dwRetVal == ERROR_NO_DATA) {
  printf("There are no network adapters with IPv4 enabled on the local system\n");
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
    (LPTSTR) &amp;lpMsgBuf,
    0,
    NULL ))  {
    printf("\tError: %s", lpMsgBuf);
  }
  LocalFree( lpMsgBuf );
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/efc0d175-2c6d-4608-b385-1623a9e0375c">GetInterfaceInfo</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/d53c3821-00a0-4eaa-9a06-69ec7aa98d84">IP Helper Structures</a>



<a href="https://msdn.microsoft.com/83d95ef3-13a4-4124-84cd-3016e9fb4446">IP_ADAPTER_INDEX_MAP</a>
 

 

