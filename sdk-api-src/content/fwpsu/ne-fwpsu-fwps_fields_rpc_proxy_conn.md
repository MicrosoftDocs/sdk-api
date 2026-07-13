---
UID: NE:fwpsu.FWPS_FIELDS_RPC_PROXY_CONN_
tech.root: fwp
title: FWPS_FIELDS_RPC_PROXY_CONN
ms.date: 06/06/2024
targetos: Windows
description: Specifies the data field identifiers for the FWPS_LAYER_RPC_PROXY_CONN run-time filtering layer.
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
 - FWPS_FIELDS_RPC_PROXY_CONN_
 - FWPS_FIELDS_RPC_PROXY_CONN
f1_keywords:
 - FWPS_FIELDS_RPC_PROXY_CONN_
 - fwpsu/FWPS_FIELDS_RPC_PROXY_CONN_
 - FWPS_FIELDS_RPC_PROXY_CONN
 - fwpsu/FWPS_FIELDS_RPC_PROXY_CONN
dev_langs:
 - c++
helpviewer_keywords:
 - FWPS_FIELDS_RPC_PROXY_CONN_
---

## -description

Specifies the data field identifiers for the [FWPS_LAYER_RPC_PROXY_CONN](./ne-fwpsu-fwps_builtin_layers.md) run-time filtering layer.

## -enum-fields

### -field FWPS_FIELD_RPC_PROXY_CONN_CLIENT_TOKEN

The identification of the client when using RpcProxy.

### -field FWPS_FIELD_RPC_PROXY_CONN_SERVER_NAME

The name of the RPC server when using RpcProxy.

### -field FWPS_FIELD_RPC_PROXY_CONN_SERVER_PORT

The port on the RPC server when using RpcProxy.

### -field FWPS_FIELD_RPC_PROXY_CONN_PROXY_AUTH_TYPE

The RPC proxy authentication service type. For more information about authentication service
types, see Authentication-Service Constants in the RPC section of the Windows SDK.

### -field FWPS_FIELD_RPC_PROXY_CONN_CLIENT_CERT_KEY_LENGTH

The secure socket layer (SSL) key length in the client certificate.

### -field FWPS_FIELD_RPC_PROXY_CONN_CLIENT_CERT_OID

The object identifier (OID) in the client certificate.

### -field FWPS_FIELD_RPC_PROXY_CONN_MAX

The maximum value for this enumeration. This value might change in future versions of the NDIS
header files and binaries.

## -remarks

## -see-also
