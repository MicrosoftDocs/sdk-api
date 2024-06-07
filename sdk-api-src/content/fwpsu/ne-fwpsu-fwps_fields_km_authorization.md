---
UID: NE:fwpsu.FWPS_FIELDS_KM_AUTHORIZATION_
tech.root: fwp
title: FWPS_FIELDS_KM_AUTHORIZATION
ms.date: 06/05/2024
targetos: Windows
description: Specifies the data field identifiers for the FWPS_LAYER_KM_AUTHORIZATION run-time filtering layer.
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
 - FWPS_FIELDS_KM_AUTHORIZATION_
 - FWPS_FIELDS_KM_AUTHORIZATION
f1_keywords:
 - FWPS_FIELDS_KM_AUTHORIZATION_
 - fwpsu/FWPS_FIELDS_KM_AUTHORIZATION_
 - FWPS_FIELDS_KM_AUTHORIZATION
 - fwpsu/FWPS_FIELDS_KM_AUTHORIZATION
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_FIELDS_KM_AUTHORIZATION_
---

## -description

Specifies the data field identifiers for the [FWPS_LAYER_KM_AUTHORIZATION](./ne-fwpsu-fwps_builtin_layers.md) run-time filtering layer.

## -enum-fields

### -field FWPS_FIELD_KM_AUTHORIZATION_REMOTE_ID

The peer's identifier. This can be the User or Machine Token depending on the type, auth type, and
mode.

### -field FWPS_FIELD_KM_AUTHORIZATION_AUTHENTICATION_TYPE

The type of authentication used.

### -field FWPS_FIELD_KM_AUTHORIZATION_KM_TYPE

The type of Keying Module (KM) used.

### -field FWPS_FIELD_KM_AUTHORIZATION_DIRECTION

The possible values are **FWP_DIRECTION_INBOUND** and **FWP_DIRECTION_OUTBOUND**.

### -field FWPS_FIELD_KM_AUTHORIZATION_KM_MODE

The authorization mode.

### -field FWPS_FIELD_KM_AUTHORIZATION_IPSEC_POLICY_KEY

The associated IPsec policy key.

### -field FWPS_FIELD_KM_AUTHORIZATION_NAP_CONTEXT

The Network Access Protection (NAP) certificate context.

### -field FWPS_FIELD_KM_AUTHORIZATION_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
header files and binaries.

## -remarks

## -see-also
