---
UID: NE:netcon.tagNETCON_CHARACTERISTIC_FLAGS
title: NETCON_CHARACTERISTIC_FLAGS
author: windows-sdk-content
description: The NETCON_CHARACTERISTIC_FLAGS enumeration type specifies possible characteristics for a network connection.
old-location: ics\netcon_characteristic_flags.htm
tech.root: ics
ms.assetid: fc64c840-7f88-4d81-910b-3cf21dce70fa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NCCF_ALLOW_DUPLICATION, NCCF_ALLOW_REMOVAL, NCCF_ALLOW_RENAME, NCCF_ALL_USERS, NCCF_BLUETOOTH_MASK, NCCF_BRANDED, NCCF_BRIDGED, NCCF_DEFAULT, NCCF_FIREWALLED, NCCF_HOMENET_CAPABLE, NCCF_INCOMING_ONLY, NCCF_LAN_MASK, NCCF_NONE, NCCF_OUTGOING_ONLY, NCCF_QUARANTINED, NCCF_RESERVED, NCCF_SHARED, NCCF_SHARED_PRIVATE, NETCON_CHARACTERISTIC_FLAGS, NETCON_CHARACTERISTIC_FLAGS enumeration [ICS/ICF], _ics_netcon_characteristic_flags, ics.netcon_characteristic_flags, netcon/NCCF_ALLOW_DUPLICATION, netcon/NCCF_ALLOW_REMOVAL, netcon/NCCF_ALLOW_RENAME, netcon/NCCF_ALL_USERS, netcon/NCCF_BLUETOOTH_MASK, netcon/NCCF_BRANDED, netcon/NCCF_BRIDGED, netcon/NCCF_DEFAULT, netcon/NCCF_FIREWALLED, netcon/NCCF_HOMENET_CAPABLE, netcon/NCCF_INCOMING_ONLY, netcon/NCCF_LAN_MASK, netcon/NCCF_NONE, netcon/NCCF_OUTGOING_ONLY, netcon/NCCF_QUARANTINED, netcon/NCCF_RESERVED, netcon/NCCF_SHARED, netcon/NCCF_SHARED_PRIVATE, netcon/NETCON_CHARACTERISTIC_FLAGS
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
 - NETCON_CHARACTERISTIC_FLAGS
product: Windows
targetos: Windows
req.typenames: NETCON_CHARACTERISTIC_FLAGS
req.redist: 
---

# NETCON_CHARACTERISTIC_FLAGS enumeration


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
 

 

