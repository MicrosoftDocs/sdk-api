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

# LPDHCP_CONTROL callback function


## -description


The 
<b>DhcpControlHook</b> function is called by Microsoft DHCP Server when the DHCP Server service is started, stopped, paused, or continued. The 
<b>DhcpControlHook</b> is implemented by a third-party DLL that registers for notification of significant Microsoft DHCP Server events. The 
<b>DhcpControlHook</b> function should not block.


## -parameters




### -param dwControlCode [in]

Specifies the control event that triggered the notification. This parameter will be one of the following: 




<ul>
<li>DHCP_CONTROL_START</li>
<li>DHCP_CONTROL_STOP</li>
<li>DHCP_CONTROL_PAUSE</li>
<li>DHCP_CONTROL_CONTINUE</li>
</ul>

### -param lpReserved [in]

Reserved for future use.


## -returns



Return values are defined by the application providing the callback.




## -remarks



This routine should not block.




## -see-also




<a href="https://msdn.microsoft.com/fa57e5c5-2335-44ba-8642-61dcb8b33ffe">DHCP_CALLOUT_TABLE</a>



<a href="https://msdn.microsoft.com/a80c2cd3-291d-4646-9dba-20a42e78dee5">DhcpServerCalloutEntry</a>



<a href="https://msdn.microsoft.com/35ec953e-0345-4c18-8790-33da189c6a43">How the
		  DHCP Server API Operates</a>
 

 

