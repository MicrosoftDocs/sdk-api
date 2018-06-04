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

# tagNETCON_STATUS enumeration


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

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




<a href="https://msdn.microsoft.com/7dd55645-c8e6-4ebd-9bf6-3bc3b3f5166f">INetConnection</a>



<a href="https://msdn.microsoft.com/fa6cc803-06f5-4b5c-98a5-c37dae08650f">Internet Connection Sharing and Internet Connection Firewall Enumeration Types</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>



<a href="https://msdn.microsoft.com/5acda2b8-960f-41ef-9ff2-49787f4e1c0c">NETCON_PROPERTIES</a>
 

 

