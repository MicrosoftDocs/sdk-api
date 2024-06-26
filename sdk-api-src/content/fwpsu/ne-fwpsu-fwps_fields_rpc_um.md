---
UID: NE:fwpsu.FWPS_FIELDS_RPC_UM_
tech.root: fwp
title: FWPS_FIELDS_RPC_UM
ms.date: 06/06/2024
targetos: Windows
description: Specifies the data field identifiers for the FWPS_LAYER_RPC_UM run-time filtering layer.
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
 - FWPS_FIELDS_RPC_UM_
 - FWPS_FIELDS_RPC_UM
f1_keywords:
 - FWPS_FIELDS_RPC_UM_
 - fwpsu/FWPS_FIELDS_RPC_UM_
 - FWPS_FIELDS_RPC_UM
 - fwpsu/FWPS_FIELDS_RPC_UM
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_FIELDS_RPC_UM_
---

## -description

Specifies the data field identifiers for the [FWPS_LAYER_RPC_UM](./ne-fwpsu-fwps_builtin_layers.md) run-time filtering layer.

## -enum-fields

### -field FWPS_FIELD_RPC_UM_REMOTE_USER_TOKEN

The identification of the remote user.

### -field FWPS_FIELD_RPC_UM_IF_UUID

The UUID of the RPC interface.

### -field FWPS_FIELD_RPC_UM_IF_VERSION

The version of the RPC interface.

### -field FWPS_FIELD_RPC_UM_IF_FLAG

Reserved for internal use.

### -field FWPS_FIELD_RPC_UM_DCOM_APP_ID

The identification of the COM application.

### -field FWPS_FIELD_RPC_UM_IMAGE_NAME

The name of the application.

### -field FWPS_FIELD_RPC_UM_PROTOCOL

The possible condition values are **RPC_PROTSEQ_TCP**, **RPC_PROTSEQ_HTTP**, and **RPC_PROTSEQ_NMP**.

### -field FWPS_FIELD_RPC_UM_AUTH_TYPE

The authentication service type. For more information about authentication service types, see
Authentication-Service Constants in the RPC section of the Microsoft Windows SDK documentation.

### -field FWPS_FIELD_RPC_UM_AUTH_LEVEL

The authentication service level. For more information about authentication service levels, see
Authentication-Service Constants in the RPC section of the Windows SDK documentation.

### -field FWPS_FIELD_RPC_UM_SEC_ENCRYPT_ALGORITHM

The certificate-based security service provider interface (SSPI) encryption algorithm.

### -field FWPS_FIELD_RPC_UM_SEC_KEY_SIZE

The certificate-based SSPI encryption key size.

### -field FWPS_FIELD_RPC_UM_LOCAL_ADDR_V4

The local IPv4 address.

### -field FWPS_FIELD_RPC_UM_LOCAL_ADDR_V6

The local IPv6 address.

### -field FWPS_FIELD_RPC_UM_LOCAL_PORT

The local transport protocol port number.

### -field FWPS_FIELD_RPC_UM_PIPE

The name of the remote named pipe.

### -field FWPS_FIELD_RPC_UM_REMOTE_ADDR_V4

The remote IPv4 address.

### -field FWPS_FIELD_RPC_UM_REMOTE_ADDR_V6

The remote IPv6 address. The IPv6 address of the RPC client.

### -field FWPS_FIELD_RPC_UM_RPC_OPNUM

The operation number of the RPC call.

### -field FWPS_FIELD_RPC_UM_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
header files and binaries.

## -remarks

## -see-also
