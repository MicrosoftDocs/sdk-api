---
UID: NE:netcon.tagNETCON_CHARACTERISTIC_FLAGS
title: NETCON_CHARACTERISTIC_FLAGS (netcon.h)
description: The NETCON_CHARACTERISTIC_FLAGS enumeration type specifies possible characteristics for a network connection.
helpviewer_keywords: ["NCCF_ALLOW_DUPLICATION","NCCF_ALLOW_REMOVAL","NCCF_ALLOW_RENAME","NCCF_ALL_USERS","NCCF_BLUETOOTH_MASK","NCCF_BRANDED","NCCF_BRIDGED","NCCF_DEFAULT","NCCF_FIREWALLED","NCCF_HOMENET_CAPABLE","NCCF_INCOMING_ONLY","NCCF_LAN_MASK","NCCF_NONE","NCCF_OUTGOING_ONLY","NCCF_QUARANTINED","NCCF_RESERVED","NCCF_SHARED","NCCF_SHARED_PRIVATE","NETCON_CHARACTERISTIC_FLAGS","NETCON_CHARACTERISTIC_FLAGS enumeration [ICS/ICF]","_ics_netcon_characteristic_flags","ics.netcon_characteristic_flags","netcon/NCCF_ALLOW_DUPLICATION","netcon/NCCF_ALLOW_REMOVAL","netcon/NCCF_ALLOW_RENAME","netcon/NCCF_ALL_USERS","netcon/NCCF_BLUETOOTH_MASK","netcon/NCCF_BRANDED","netcon/NCCF_BRIDGED","netcon/NCCF_DEFAULT","netcon/NCCF_FIREWALLED","netcon/NCCF_HOMENET_CAPABLE","netcon/NCCF_INCOMING_ONLY","netcon/NCCF_LAN_MASK","netcon/NCCF_NONE","netcon/NCCF_OUTGOING_ONLY","netcon/NCCF_QUARANTINED","netcon/NCCF_RESERVED","netcon/NCCF_SHARED","netcon/NCCF_SHARED_PRIVATE","netcon/NETCON_CHARACTERISTIC_FLAGS"]
old-location: ics\netcon_characteristic_flags.htm
tech.root: ics
ms.assetid: fc64c840-7f88-4d81-910b-3cf21dce70fa
ms.date: 12/05/2018
ms.keywords: NCCF_ALLOW_DUPLICATION, NCCF_ALLOW_REMOVAL, NCCF_ALLOW_RENAME, NCCF_ALL_USERS, NCCF_BLUETOOTH_MASK, NCCF_BRANDED, NCCF_BRIDGED, NCCF_DEFAULT, NCCF_FIREWALLED, NCCF_HOMENET_CAPABLE, NCCF_INCOMING_ONLY, NCCF_LAN_MASK, NCCF_NONE, NCCF_OUTGOING_ONLY, NCCF_QUARANTINED, NCCF_RESERVED, NCCF_SHARED, NCCF_SHARED_PRIVATE, NETCON_CHARACTERISTIC_FLAGS, NETCON_CHARACTERISTIC_FLAGS enumeration [ICS/ICF], _ics_netcon_characteristic_flags, ics.netcon_characteristic_flags, netcon/NCCF_ALLOW_DUPLICATION, netcon/NCCF_ALLOW_REMOVAL, netcon/NCCF_ALLOW_RENAME, netcon/NCCF_ALL_USERS, netcon/NCCF_BLUETOOTH_MASK, netcon/NCCF_BRANDED, netcon/NCCF_BRIDGED, netcon/NCCF_DEFAULT, netcon/NCCF_FIREWALLED, netcon/NCCF_HOMENET_CAPABLE, netcon/NCCF_INCOMING_ONLY, netcon/NCCF_LAN_MASK, netcon/NCCF_NONE, netcon/NCCF_OUTGOING_ONLY, netcon/NCCF_QUARANTINED, netcon/NCCF_RESERVED, netcon/NCCF_SHARED, netcon/NCCF_SHARED_PRIVATE, netcon/NETCON_CHARACTERISTIC_FLAGS
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
targetos: Windows
req.typenames: NETCON_CHARACTERISTIC_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNETCON_CHARACTERISTIC_FLAGS
 - netcon/tagNETCON_CHARACTERISTIC_FLAGS
 - NETCON_CHARACTERISTIC_FLAGS
 - netcon/NETCON_CHARACTERISTIC_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NetCon.h
api_name:
 - NETCON_CHARACTERISTIC_FLAGS
---

# NETCON_CHARACTERISTIC_FLAGS enumeration


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>NETCON_CHARACTERISTIC_FLAGS</b> enumeration type specifies possible characteristics for a network connection.

## -enum-fields

### -field NCCF_NONE:0

No special characteristics.

### -field NCCF_ALL_USERS:0x1

Connection is available to all users.

### -field NCCF_ALLOW_DUPLICATION:0x2

Connection is duplicable.

### -field NCCF_ALLOW_REMOVAL:0x4

Connection is removable.

### -field NCCF_ALLOW_RENAME:0x8

Connection can be renamed.

### -field NCCF_INCOMING_ONLY:0x20

Direction is "incoming" only.

### -field NCCF_OUTGOING_ONLY:0x40

Direction is "outgoing" only.

### -field NCCF_BRANDED:0x80

Icons are branded.

### -field NCCF_SHARED:0x100

Connection is shared.

### -field NCCF_BRIDGED:0x200

Connection is bridged.

### -field NCCF_FIREWALLED:0x400

Connection is firewalled.

### -field NCCF_DEFAULT:0x800

Connection is the default connection.

### -field NCCF_HOMENET_CAPABLE:0x1000

Device supports home networking.

### -field NCCF_SHARED_PRIVATE:0x2000

Connection is private (part of ICS).

### -field NCCF_QUARANTINED:0x4000

Connection is quarantined.

### -field NCCF_RESERVED:0x8000

Unused.

### -field NCCF_HOSTED_NETWORK:0x10000

### -field NCCF_VIRTUAL_STATION:0x20000

### -field NCCF_WIFI_DIRECT:0x40000

### -field NCCF_BLUETOOTH_MASK:0xf0000

Bluetooth characteristics.

### -field NCCF_LAN_MASK:0xf00000

LAN characteristics.

## -see-also

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetconnection">INetConnection</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-enumeration-types">Internet Connection Sharing and Internet Connection Firewall Enumeration Types</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>



<a href="/windows/desktop/api/netcon/ns-netcon-netcon_properties">NETCON_PROPERTIES</a>
