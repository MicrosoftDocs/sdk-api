---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

