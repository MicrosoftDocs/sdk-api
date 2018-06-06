---
UID: NS:dhcpssdk._DHCP_CALLOUT_TABLE
title: "_DHCP_CALLOUT_TABLE"
author: windows-sdk-content
description: The DHCP_CALLOUT_TABLE structure is used by Microsoft DHCP Server and third-party DLLs to send notification requests for DHCP Server events.
old-location: dhcp\dhcp_callout_table.htm
old-project: DHCP
ms.assetid: fa57e5c5-2335-44ba-8642-61dcb8b33ffe
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*LPDHCP_CALLOUT_TABLE, DHCP_CALLOUT_TABLE, DHCP_CALLOUT_TABLE structure [DHCP], LPDHCP_CALLOUT_TABLE, LPDHCP_CALLOUT_TABLE structure pointer [DHCP], _DHCP_CALLOUT_TABLE, _dhcp_dhcp_callout_table, dhcp.dhcp_callout_table, dhcpssdk/DHCP_CALLOUT_TABLE, dhcpssdk/LPDHCP_CALLOUT_TABLE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DHCP_CALLOUT_TABLE, *LPDHCP_CALLOUT_TABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpssdk.h
api_name:
 - DHCP_CALLOUT_TABLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCP_CALLOUT_TABLE structure


## -description


The 
<b>DHCP_CALLOUT_TABLE</b> structure is used by Microsoft DHCP Server and third-party DLLs to send notification requests for DHCP Server events.


## -struct-fields




### -field DhcpControlHook

Pointer to a 
<a href="https://msdn.microsoft.com/28019037-15ed-4d72-bd85-d6aca3c3ca75">DhcpControlHook</a> function, implemented in a third-party DLL, to be called when Microsoft DHCP Server is started, stopped, paused, or continued. Set to <b>NULL</b> if notification is not required.


### -field DhcpNewPktHook

Pointer to a 
<a href="https://msdn.microsoft.com/2bff8750-aeb2-4164-9a6e-4239a6736beb">DhcpNewPktHook</a> function, implemented in a third-party DLL, to be called when Microsoft DHCP Server receives a packet that it attempts to process. Set to <b>NULL</b> if notification is not required.


### -field DhcpPktDropHook

Pointer to a 
<a href="https://msdn.microsoft.com/29fa3266-a0a7-4e17-bf15-35a454f78b12">DhcpPktDropHook</a> function, implemented in a third-party DLL, to be called when Microsoft DHCP Server drops a packet, and when a packet is completely processed by Microsoft DHCP Server. Set to <b>NULL</b> if notification is not required.


### -field DhcpPktSendHook

Pointer to a 
<a href="https://msdn.microsoft.com/0db450ea-3e14-4476-83cb-4a3a81832e57">DhcpPktSendHook</a> function, implemented in a third-party DLL, to be called directly before Microsoft DHCP Server submits a response to a client inquiry. Set to <b>NULL</b> if notification is not required.


### -field DhcpAddressDelHook

Pointer to a 
<a href="https://msdn.microsoft.com/fd9ce5df-927d-4b34-9561-ff5a2ebad16e">DhcpAddressDelHook</a> function, implemented in a third-party DLL, to be called when a specified event in Microsoft DHCP Server results in a packet being dropped. Set to <b>NULL</b> if notification is not required.


### -field DhcpAddressOfferHook

Pointer to a 
<a href="https://msdn.microsoft.com/1c122657-a92a-4232-879a-12105dc967e1">DhcpAddressOfferHook</a> function, implemented in a third-party DLL, to be called directly before Microsoft DHCP Server submits a DHCP ACK message in response to a DHCP REQUEST message. Set to <b>NULL</b> if notification is not required.


### -field DhcpHandleOptionsHook

Pointer to a 
<a href="https://msdn.microsoft.com/51bb3d2c-953d-446a-ad70-eb6cc8d4dbca">DhcpHandleOptionsHook</a> function, implemented in a third-party DLL, that sends only parsed DHCP information to the third-party DLL, enabling the third-party DLL to avoid processing the entire DHCP packet. Set to <b>NULL</b> if notification is not required.


### -field DhcpDeleteClientHook

Pointer to a 
<a href="https://msdn.microsoft.com/ae92436c-0774-4664-86ac-c7df65ef40b5">DhcpDeleteClientHook</a> function, implemented in a third-party DLL, to be called directly before Microsoft DHCP Server deletes a client lease from its active leases database. Set to <b>NULL</b> if notification is not required.


### -field DhcpExtensionHook

Reserved for future use.


### -field DhcpReservedHook

Reserved for future use.


## -remarks



It is not necessary to implement all hooks available from Microsoft DHCP Server. If notification for a particular event is not required, set the member to <b>NULL</b>. Remember, however, that the initially loaded third-party DLL is responsible for loading subsequent third-party DLLs, and that subsequent DLLs may require notification of events that otherwise would be <b>NULL</b>, resulting in a non-<b>NULL</b> setting for members used by chained third-party DLLs that would otherwise be unused.




## -see-also




<a href="https://msdn.microsoft.com/782dd73a-7f32-4001-859b-21379f1e80d4">Chaining Multiple Third-Party DLLs</a>



<a href="https://msdn.microsoft.com/fd9ce5df-927d-4b34-9561-ff5a2ebad16e">DhcpAddressDelHook</a>



<a href="https://msdn.microsoft.com/1c122657-a92a-4232-879a-12105dc967e1">DhcpAddressOfferHook</a>



<a href="https://msdn.microsoft.com/28019037-15ed-4d72-bd85-d6aca3c3ca75">DhcpControlHook</a>



<a href="https://msdn.microsoft.com/ae92436c-0774-4664-86ac-c7df65ef40b5">DhcpDeleteClientHook</a>



<a href="https://msdn.microsoft.com/51bb3d2c-953d-446a-ad70-eb6cc8d4dbca">DhcpHandleOptionsHook</a>



<a href="https://msdn.microsoft.com/2bff8750-aeb2-4164-9a6e-4239a6736beb">DhcpNewPktHook</a>



<a href="https://msdn.microsoft.com/29fa3266-a0a7-4e17-bf15-35a454f78b12">DhcpPktDropHook</a>



<a href="https://msdn.microsoft.com/0db450ea-3e14-4476-83cb-4a3a81832e57">DhcpPktSendHook</a>



<a href="https://msdn.microsoft.com/a80c2cd3-291d-4646-9dba-20a42e78dee5">DhcpServerCalloutEntry</a>
 

 

