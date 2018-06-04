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

# AllocateAndGetUdpExTableFromStack function


## -description


<p class="CCE_Message">[This function is no longer available for use as of Windows Vista. Instead, use the <a href="https://msdn.microsoft.com/00e80e90-1a6d-426d-90cd-20b967ebbb8e">GetUdpTable</a> or <a href="https://msdn.microsoft.com/c936d5a0-ca5e-487e-b304-bfd81403ab40">GetExtendedUdpTable</a> function to retrieve the UDP connection table.]

The <b>AllocateAndGetUdpExTableFromStack</b> function retrieves the UDP connection table and allocates memory from the local heap to store the table.


## -parameters




### -param ppUdpTable

TBD


### -param bOrder [in]

If true, the UDP connection entries in the table returned in <i>ppUDPTable</i> are sorted; if false, they are not.


### -param hHeap [in]

Handle to the heap from which the memory to store the table will be allocated.


### -param dwFlags [in]

One or more flags that indicate specific heap allocation control behaviors.


### -param dwFamily [in]

The family of the UDP addresses in the table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
</dl>
</td>
<td width="60%">
Retrieve IPv4 UDP addresses.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
</dl>
</td>
<td width="60%">
Retrieve IPv6 UDP addresses.

</td>
</tr>
</table>
 


#### - ppUDPTable [out]

Pointer to the address of the opaque data that contains the UDP connection table after the function returns.


## -returns



If the function succeeds, it returns ERROR_SUCCESS.

If the function fails, it returns a function from winerror.h.




## -remarks



In the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the function prototype for <b>AllocateAndGetUdpExTableFromStack</b> is still defined in the Iphlpapi.h header file for continued support on Windows Server 2003 and Windows XP.




## -see-also




<a href="https://msdn.microsoft.com/c79dd5ba-e80b-494f-80fa-efa10c021773">AllocateAndGetTcpExTableFromStack</a>



<a href="https://msdn.microsoft.com/c936d5a0-ca5e-487e-b304-bfd81403ab40">GetExtendedUdpTable</a>



<a href="https://msdn.microsoft.com/00e80e90-1a6d-426d-90cd-20b967ebbb8e">GetUdpTable</a>
 

 

