---
UID: NC:dhcpssdk.LPDHCP_CONTROL
title: LPDHCP_CONTROL (dhcpssdk.h)
description: The DhcpControlHook function is called by Microsoft DHCP Server when the DHCP Server service is started, stopped, paused, or continued.
helpviewer_keywords: ["DhcpControlHook","DhcpControlHook callback function [DHCP]","LPDHCP_CONTROL","LPDHCP_CONTROL callback","_dhcp_dhcpcontrolhook","dhcp.dhcpcontrolhook","dhcpssdk/DhcpControlHook"]
old-location: dhcp\dhcpcontrolhook.htm
tech.root: DHCP
ms.assetid: 28019037-15ed-4d72-bd85-d6aca3c3ca75
ms.date: 12/05/2018
ms.keywords: DhcpControlHook, DhcpControlHook callback function [DHCP], LPDHCP_CONTROL, LPDHCP_CONTROL callback, _dhcp_dhcpcontrolhook, dhcp.dhcpcontrolhook, dhcpssdk/DhcpControlHook
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPDHCP_CONTROL
 - dhcpssdk/LPDHCP_CONTROL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Dhcpssdk.h
api_name:
 - DhcpControlHook
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

<a href="/windows/desktop/api/dhcpssdk/ns-dhcpssdk-dhcp_callout_table">DHCP_CALLOUT_TABLE</a>



<a href="/previous-versions/windows/desktop/api/dhcpssdk/nc-dhcpssdk-lpdhcp_entry_point_func">DhcpServerCalloutEntry</a>



<a href="/previous-versions/windows/desktop/dhcp/how-the-dhcp-server-api-operates">How the
		  DHCP Server API Operates</a>