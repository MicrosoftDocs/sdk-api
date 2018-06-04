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

# DhcpDeRegisterParamChange function


## -description


The 
<b>DhcpDeRegisterParamChange</b> function releases resources associated with previously registered event notifications, and closes the associated event handle.


## -parameters




### -param Flags [in]

Reserved. Must be set to zero.


### -param Reserved [in]

Reserved. Must be set to <b>NULL</b>.


### -param Event [in]

Must be the same value as the <b>HANDLE</b> variable in the 
<a href="https://msdn.microsoft.com/e0099827-2f88-4309-a5e7-3bc1395de5a2">DhcpRegisterParamChange</a> function call for which the client is deregistering event notification.


## -returns



Returns ERROR_SUCCESS upon successful completion. Otherwise, returns Windows error codes.




## -remarks



The 
<b>DhcpDeRegisterParamChange</b> function must be made subsequent to an associated 
<a href="https://msdn.microsoft.com/e0099827-2f88-4309-a5e7-3bc1395de5a2">DhcpRegisterParamChange</a> function call, and the <i>Flags</i> parameter and the <b>HANDLE</b> variable passed  
in the <i>Event</i> parameter to <b>DhcpDeRegisterParamChange</b> must match corresponding <i>Flags</i> parameter and the <b>HANDLE</b> variable of the previous and associated 
<b>DhcpRegisterParamChange</b> function call.




## -see-also




<a href="https://msdn.microsoft.com/ca859a72-51d3-4bd5-96b9-7a9a2df95595">DHCP Functions</a>



<a href="https://msdn.microsoft.com/b4bc8b02-63b4-4751-a963-25336e8ae426">DhcpCApiInitialize</a>



<a href="https://msdn.microsoft.com/e0099827-2f88-4309-a5e7-3bc1395de5a2">DhcpRegisterParamChange</a>
 

 

