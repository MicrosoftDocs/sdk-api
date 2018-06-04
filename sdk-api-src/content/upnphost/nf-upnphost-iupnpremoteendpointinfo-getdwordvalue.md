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

# IUPnPRemoteEndpointInfo::GetDwordValue


## -description


The <b>GetDwordValue</b> method gets a 4-byte value that provides information about either a request or requester.


## -parameters




### -param bstrValueName [in]

String that specifies the category of information to be retrieved.


### -param pdwValue [out]

Pointer to a 4-byte value, the meaning of which depends on the value of <i>bstrValueName</i>.

If <i>bstrValueName</i> is "AddressFamily", the 4-byte value indicates the format of the requester's IP address as follows. The values are defined in Winsock2.h.

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
IP (IP version 4)

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
</dl>
</td>
<td width="60%">
IP6 (IP version 6)

</td>
</tr>
</table>
 


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



Currently, the only valid value for the <i>bstrValueName</i> parameter is "AddressFamily". For any other value, this method will return the COM error code E_INVALIDARG.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597612">GetGuidValue</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff597621">GetStringValue</a>



<a href="https://msdn.microsoft.com/32e246cd-50eb-4221-8166-a7cd8ed42d69">IUPnPRemoteEndpointInfo</a>
 

 

