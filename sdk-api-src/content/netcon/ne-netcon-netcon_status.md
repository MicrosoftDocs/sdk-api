---
UID: NE:netcon.tagNETCON_STATUS
title: NETCON_STATUS (netcon.h)
author: windows-sdk-content
description: The NETCON_STATUS type enumerates possible status conditions for a network connection.
old-location: ics\netcon_status.htm
tech.root: ics
ms.assetid: feb0aa60-b873-4536-8ec2-2dce4d355fdb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NCS_AUTHENTICATING, NCS_AUTHENTICATION_FAILED, NCS_AUTHENTICATION_SUCCEEDED, NCS_CONNECTED, NCS_CONNECTING, NCS_CREDENTIALS_REQUIRED, NCS_DISCONNECTED, NCS_DISCONNECTING, NCS_HARDWARE_DISABLED, NCS_HARDWARE_MALFUNCTION, NCS_HARDWARE_NOT_PRESENT, NCS_INVALID_ADDRESS, NCS_MEDIA_DISCONNECTED, NETCON_STATUS, NETCON_STATUS enumeration [ICS/ICF], _ics_netcon_status, ics.netcon_status, netcon/NCS_AUTHENTICATING, netcon/NCS_AUTHENTICATION_FAILED, netcon/NCS_AUTHENTICATION_SUCCEEDED, netcon/NCS_CONNECTED, netcon/NCS_CONNECTING, netcon/NCS_CREDENTIALS_REQUIRED, netcon/NCS_DISCONNECTED, netcon/NCS_DISCONNECTING, netcon/NCS_HARDWARE_DISABLED, netcon/NCS_HARDWARE_MALFUNCTION, netcon/NCS_HARDWARE_NOT_PRESENT, netcon/NCS_INVALID_ADDRESS, netcon/NCS_MEDIA_DISCONNECTED, netcon/NETCON_STATUS
ms.topic: enum
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
 - HeaderDef
api_location:
 - NetCon.h
api_name:
 - NETCON_STATUS
product: Windows
targetos: Windows
req.typenames: NETCON_STATUS
req.redist: 
---

# NETCON_STATUS enumeration


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/en-us/library/Aa366453(v=VS.85).aspx">Windows Firewall API</a>.]

The 
<b>NETCON_STATUS</b> type enumerates possible status conditions for a network connection.


## -enum-fields




### -field NCS_DISCONNECTED

The connection is disconnected.


### -field NCS_CONNECTING

The connection is in the process of connecting.


### -field NCS_CONNECTED

The connection is in a connected state.


### -field NCS_DISCONNECTING

The connection is in the process of disconnecting.


### -field NCS_HARDWARE_NOT_PRESENT

The hardware for the connection, for example network interface card (NIC), is not present.


### -field NCS_HARDWARE_DISABLED

The hardware for the connection is present, but is not enabled.


### -field NCS_HARDWARE_MALFUNCTION

A malfunction has occurred in the hardware for the connection.


### -field NCS_MEDIA_DISCONNECTED

The media, for example the network cable, is disconnected.


### -field NCS_AUTHENTICATING

The connection is waiting for authentication to occur.


### -field NCS_AUTHENTICATION_SUCCEEDED

Authentication has succeeded on this connection.


### -field NCS_AUTHENTICATION_FAILED

Authentication has failed on this connection.


### -field NCS_INVALID_ADDRESS

The address is invalid.


### -field NCS_CREDENTIALS_REQUIRED

Security credentials are required.


### -field NCS_ACTION_REQUIRED


### -field NCS_ACTION_REQUIRED_RETRY


### -field NCS_CONNECT_FAILED




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa365084(v=VS.85).aspx">INetConnection</a>



<a href="https://msdn.microsoft.com/fa6cc803-06f5-4b5c-98a5-c37dae08650f">Internet Connection Sharing and Internet Connection Firewall Enumeration Types</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>



<a href="https://msdn.microsoft.com/5acda2b8-960f-41ef-9ff2-49787f4e1c0c">NETCON_PROPERTIES</a>
 

 

