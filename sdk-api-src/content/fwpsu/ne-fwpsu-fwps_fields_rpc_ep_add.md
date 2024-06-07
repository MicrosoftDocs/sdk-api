---
UID: NE:fwpsu.FWPS_FIELDS_RPC_EP_ADD_
tech.root: fwp
title: FWPS_FIELDS_RPC_EP_ADD
ms.date: 06/06/2024
targetos: Windows
description: Specifies the data field identifiers for the FWPS_LAYER_RPC_EP_ADD run-time filtering layer.
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
 - FWPS_FIELDS_RPC_EP_ADD_
 - FWPS_FIELDS_RPC_EP_ADD
f1_keywords:
 - FWPS_FIELDS_RPC_EP_ADD_
 - fwpsu/FWPS_FIELDS_RPC_EP_ADD_
 - FWPS_FIELDS_RPC_EP_ADD
 - fwpsu/FWPS_FIELDS_RPC_EP_ADD
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_FIELDS_RPC_EP_ADD_
---

## -description

Specifies the data field identifiers for the [FWPS_LAYER_RPC_EP_ADD](./ne-fwpsu-fwps_builtin_layers.md) run-time filtering layer.

## -enum-fields

### -field FWPS_FIELD_RPC_EP_ADD_PROCESS_WITH_RPC_IF_UUID

The UUID of the process with the RPC interface.

### -field FWPS_FIELD_RPC_EP_ADD_PROTOCOL

The possible condition values are **RPC_PROTSEQ_TCP**, **RPC_PROTSEQ_HTTP**, and **RPC_PROTSEQ_NMP**.

### -field FWPS_FIELD_RPC_EP_ADD_EP_VALUE

Reserved for internal use.

### -field FWPS_FIELD_RPC_EP_ADD_EP_FLAGS

Reserved for internal use.

### -field FWPS_FIELD_RPC_EP_ADD_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
header files and binaries.

## -remarks

## -see-also
