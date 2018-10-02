---
UID: NC:dhcpssdk.LPDHCP_CONTROL
title: LPDHCP_CONTROL
author: windows-sdk-content
description: The DhcpControlHook function is called by Microsoft DHCP Server when the DHCP Server service is started, stopped, paused, or continued.
old-location: dhcp\dhcpcontrolhook.htm
tech.root: DHCP
ms.assetid: 28019037-15ed-4d72-bd85-d6aca3c3ca75
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DhcpControlHook, DhcpControlHook callback function [DHCP], LPDHCP_CONTROL, LPDHCP_CONTROL callback, _dhcp_dhcpcontrolhook, dhcp.dhcpcontrolhook, dhcpssdk/DhcpControlHook
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: dhcpssdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Dhcpssdk.h
api_name:
 - DhcpControlHook
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

