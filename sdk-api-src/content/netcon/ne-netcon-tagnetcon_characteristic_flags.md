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

# tagNETCON_CHARACTERISTIC_FLAGS enumeration


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>NETCON_CHARACTERISTIC_FLAGS</b> enumeration type specifies possible characteristics for a network connection.


## -enum-fields




### -field NCCF_NONE

No special characteristics.


### -field NCCF_ALL_USERS

Connection is available to all users.


### -field NCCF_ALLOW_DUPLICATION

Connection is duplicable.


### -field NCCF_ALLOW_REMOVAL

Connection is removable.


### -field NCCF_ALLOW_RENAME

Connection can be renamed.


### -field NCCF_INCOMING_ONLY

Direction is "incoming" only.


### -field NCCF_OUTGOING_ONLY

Direction is "outgoing" only.


### -field NCCF_BRANDED

Icons are branded.


### -field NCCF_SHARED

Connection is shared.


### -field NCCF_BRIDGED

Connection is bridged.


### -field NCCF_FIREWALLED

Connection is firewalled.


### -field NCCF_DEFAULT

Connection is the default connection.


### -field NCCF_HOMENET_CAPABLE

Device supports home networking.


### -field NCCF_SHARED_PRIVATE

Connection is private (part of ICS).


### -field NCCF_QUARANTINED

Connection is quarantined.


### -field NCCF_RESERVED

Unused.


### -field NCCF_HOSTED_NETWORK


### -field NCCF_VIRTUAL_STATION


### -field NCCF_WIFI_DIRECT


### -field NCCF_BLUETOOTH_MASK

Bluetooth characteristics.


### -field NCCF_LAN_MASK

LAN characteristics.


## -see-also




<a href="https://msdn.microsoft.com/7dd55645-c8e6-4ebd-9bf6-3bc3b3f5166f">INetConnection</a>



<a href="https://msdn.microsoft.com/fa6cc803-06f5-4b5c-98a5-c37dae08650f">Internet Connection Sharing and Internet Connection Firewall Enumeration Types</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>



<a href="https://msdn.microsoft.com/5acda2b8-960f-41ef-9ff2-49787f4e1c0c">NETCON_PROPERTIES</a>
 

 

