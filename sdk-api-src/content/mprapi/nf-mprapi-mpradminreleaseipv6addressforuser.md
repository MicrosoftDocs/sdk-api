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

# MprAdminReleaseIpv6AddressForUser function


## -description


The 
<i>MprAdminReleaseIpv6AddressForUser</i> function is called once for each user that needs to release an IPv6 address.


## -parameters




### -param lpszUserName

TBD


### -param lpszPortName

TBD


### -param lpdwIpv6Address [in]

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff554787">IN6_ADDR</a> structure. This variable specifies the IPv6 address to be released.


#### - lpwszPortName [in]

Pointer to a Unicode string that specifies the name of the port on which the user disconnected.


#### - lpwszUserName [in]

Pointer to a Unicode string that specifies the name of the user that disconnected.


## -returns



If function succeeds, the return value should be NO_ERROR.

If the function returns anything other than NO_ERROR, RAS will terminate the connection.




## -remarks



An administration DLL need not implement the 
<i>MprAdminReleaseIpv6AddressForUser</i> function. However, if the DLL implements 
<i>MprAdminReleaseIpv6AddressForUser</i>, it must also implement 
<a href="https://msdn.microsoft.com/ec4b4130-4864-470f-8647-1fcadd359c58">MprAdminGetIpv6AddressForUser</a>.




## -see-also




<a href="https://msdn.microsoft.com/504ce881-7d06-41d3-a942-0fe27be12bd3">MprAdminConnectionHangupNotification</a>



<a href="https://msdn.microsoft.com/ec4b4130-4864-470f-8647-1fcadd359c58">MprAdminGetIpv6AddressForUser</a>



<a href="https://msdn.microsoft.com/c15c6e2d-3bb6-4583-9ac3-19528feb863f">RAS Administration DLL</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

