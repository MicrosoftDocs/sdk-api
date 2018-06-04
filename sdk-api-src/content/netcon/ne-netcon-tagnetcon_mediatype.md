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

# tagNETCON_MEDIATYPE enumeration


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The values of the <b>NETCON_MEDIATYPE</b> enumerate the possible ways the computer connects to the network.


## -enum-fields




### -field NCM_NONE

No media is present.


### -field NCM_DIRECT

Direct serial connection through a serial port.


### -field NCM_ISDN

Connection is through an integrated services digital network (ISDN) line.


### -field NCM_LAN

Connection is to a local area network (LAN).


### -field NCM_PHONE

Dial-up connection over a conventional phone line.


### -field NCM_TUNNEL

Virtual private network (VPN) connection.


### -field NCM_PPPOE

Point-to-Point protocol (PPP) over Ethernet.


### -field NCM_BRIDGE

Bridged connection.


### -field NCM_SHAREDACCESSHOST_LAN

Shared connection to a LAN.


### -field NCM_SHAREDACCESSHOST_RAS

Shared connection to a remote or wide area network (WAN).


## -see-also




<a href="https://msdn.microsoft.com/7dd55645-c8e6-4ebd-9bf6-3bc3b3f5166f">INetConnection</a>



<a href="https://msdn.microsoft.com/fa6cc803-06f5-4b5c-98a5-c37dae08650f">Internet Connection Sharing and Internet Connection Firewall Enumeration Types</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>



<a href="https://msdn.microsoft.com/5acda2b8-960f-41ef-9ff2-49787f4e1c0c">NETCON_PROPERTIES</a>
 

 

