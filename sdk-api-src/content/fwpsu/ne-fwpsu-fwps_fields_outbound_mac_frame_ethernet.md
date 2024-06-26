---
UID: NE:fwpsu.FWPS_FIELDS_OUTBOUND_MAC_FRAME_ETHERNET_
tech.root: fwp
title: FWPS_FIELDS_OUTBOUND_MAC_FRAME_ETHERNET
ms.date: 06/05/2024
targetos: Windows
description: Specifies the data field identifiers for the FWPS_LAYER_OUTBOUND_MAC_FRAME_ETHERNET run-time filtering layer.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: fwpsu.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: 
typedef_isUnnamed: false
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - fwpsu.h
api_name:
 - FWPS_FIELDS_OUTBOUND_MAC_FRAME_ETHERNET_
 - FWPS_FIELDS_OUTBOUND_MAC_FRAME_ETHERNET
f1_keywords:
 - FWPS_FIELDS_OUTBOUND_MAC_FRAME_ETHERNET_
 - fwpsu/FWPS_FIELDS_OUTBOUND_MAC_FRAME_ETHERNET_
 - FWPS_FIELDS_OUTBOUND_MAC_FRAME_ETHERNET
 - fwpsu/FWPS_FIELDS_OUTBOUND_MAC_FRAME_ETHERNET
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_FIELDS_OUTBOUND_MAC_FRAME_ETHERNET_
---

## -description

Specifies the data field identifiers for the [FWPS_LAYER_OUTBOUND_MAC_FRAME_ETHERNET](./ne-fwpsu-fwps_builtin_layers.md) run-time filtering layer.

> [!NOTE]
> In Windows 7 and Windows Server 2008 R2, the name of this enumeration is **FWPS_FIELDS_OUTBOUND_MAC_FRAME_802_3**.

## -enum-fields

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_ETHERNET_INTERFACE_MAC_ADDRESS

The outbound MAC frame IEEE 802.3 interface MAC address field.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_ETHERNET_MAC_LOCAL_ADDRESS

The outbound MAC frame IEEE 802.3 local MAC address field.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_ETHERNET_MAC_REMOTE_ADDRESS

The outbound MAC frame IEEE 802.3 remote MAC address field.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_ETHERNET_MAC_LOCAL_ADDRESS_TYPE

The outbound MAC frame IEEE 802.3 local MAC address type field.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_ETHERNET_MAC_REMOTE_ADDRESS_TYPE

The outbound MAC frame IEEE 802.3 remote MAC address type field.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_ETHERNET_ETHER_TYPE

The outbound MAC frame IEEE 802.3 EtherType field.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_ETHERNET_VLAN_ID

The outbound MAC frame IEEE 802.3 VLAN identifier field.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_ETHERNET_INTERFACE

The outbound MAC frame IEEE 802.3 interface field.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_ETHERNET_INTERFACE_INDEX

The outbound MAC frame IEEE 802.3 interface index field.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_ETHERNET_NDIS_PORT

The outbound MAC frame IEEE 802.3 NDIS port field.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_ETHERNET_L2_FLAGS

A bitwise OR of Layer 2 (L2) flags. For a list of filtering condition flags, see [Filtering condition flags](/windows-hardware/drivers/network/filtering-condition-flags).

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_ETHERNET_COMPARTMENT_ID

The compartment that the network interface belongs to. Windows supports use of compartments for network stack isolation. You can use this to enable a multi-tenant network stack with network namespaces in different compartments.

Supported starting with Windows 10, version 1703.

### -field FWPS_FIELD_OUTBOUND_MAC_FRAME_ETHERNET_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
header files and binaries.

## -remarks

## -see-also
