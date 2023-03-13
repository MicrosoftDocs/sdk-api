---
UID: NE:mprapi._MPRAPI_OBJECT_TYPE
title: MPRAPI_OBJECT_TYPE (mprapi.h)
description: Specifies the structure type in a MPRAPI_OBJECT_HEADER structure.
helpviewer_keywords: ["*PMPRAPI_OBJECT_TYPE","MPRAPI_OBJECT_TYPE","MPRAPI_OBJECT_TYPE enumeration [RAS]","MPRAPI_OBJECT_TYPE_AUTH_VALIDATION_OBJECT","MPRAPI_OBJECT_TYPE_MPR_SERVER_OBJECT","MPRAPI_OBJECT_TYPE_MPR_SERVER_SET_CONFIG_OBJECT","MPRAPI_OBJECT_TYPE_RAS_CONNECTION_OBJECT","MPRAPI_OBJECT_TYPE_UPDATE_CONNECTION_OBJECT","mprapi/MPRAPI_OBJECT_TYPE","mprapi/MPRAPI_OBJECT_TYPE_AUTH_VALIDATION_OBJECT","mprapi/MPRAPI_OBJECT_TYPE_MPR_SERVER_OBJECT","mprapi/MPRAPI_OBJECT_TYPE_MPR_SERVER_SET_CONFIG_OBJECT","mprapi/MPRAPI_OBJECT_TYPE_RAS_CONNECTION_OBJECT","mprapi/MPRAPI_OBJECT_TYPE_UPDATE_CONNECTION_OBJECT","rras.mprapi_object_type"]
old-location: rras\mprapi_object_type.htm
tech.root: RRAS
ms.assetid: 93d5bf41-e0ec-4dcf-b784-bbd9746f8134
ms.date: 12/05/2018
ms.keywords: '*PMPRAPI_OBJECT_TYPE, MPRAPI_OBJECT_TYPE, MPRAPI_OBJECT_TYPE enumeration [RAS], MPRAPI_OBJECT_TYPE_AUTH_VALIDATION_OBJECT, MPRAPI_OBJECT_TYPE_MPR_SERVER_OBJECT, MPRAPI_OBJECT_TYPE_MPR_SERVER_SET_CONFIG_OBJECT, MPRAPI_OBJECT_TYPE_RAS_CONNECTION_OBJECT, MPRAPI_OBJECT_TYPE_UPDATE_CONNECTION_OBJECT, mprapi/MPRAPI_OBJECT_TYPE, mprapi/MPRAPI_OBJECT_TYPE_AUTH_VALIDATION_OBJECT, mprapi/MPRAPI_OBJECT_TYPE_MPR_SERVER_OBJECT, mprapi/MPRAPI_OBJECT_TYPE_MPR_SERVER_SET_CONFIG_OBJECT, mprapi/MPRAPI_OBJECT_TYPE_RAS_CONNECTION_OBJECT, mprapi/MPRAPI_OBJECT_TYPE_UPDATE_CONNECTION_OBJECT, rras.mprapi_object_type'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: MPRAPI_OBJECT_TYPE, *PMPRAPI_OBJECT_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPRAPI_OBJECT_TYPE
 - mprapi/_MPRAPI_OBJECT_TYPE
 - PMPRAPI_OBJECT_TYPE
 - mprapi/PMPRAPI_OBJECT_TYPE
 - MPRAPI_OBJECT_TYPE
 - mprapi/MPRAPI_OBJECT_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - MPRAPI_OBJECT_TYPE
---

# MPRAPI_OBJECT_TYPE enumeration


## -description

The <b>MPRAPI_OBJECT_TYPE</b> enumeration specifies the structure type in  a <a href="/windows/desktop/api/mprapi/ns-mprapi-mprapi_object_header">MPRAPI_OBJECT_HEADER</a> structure.

## -enum-fields

### -field MPRAPI_OBJECT_TYPE_RAS_CONNECTION_OBJECT:1

The structure is a <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_ex">RAS_CONNECTION_EX</a> structure.

### -field MPRAPI_OBJECT_TYPE_MPR_SERVER_OBJECT:2

The structure is a <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_ex0">MPR_SERVER_EX</a> structure.

### -field MPRAPI_OBJECT_TYPE_MPR_SERVER_SET_CONFIG_OBJECT:3

The structure is a <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_set_config_ex0">MPR_SERVER_SET_CONFIG_EX</a> structure.

### -field MPRAPI_OBJECT_TYPE_AUTH_VALIDATION_OBJECT:4

The structure is a <a href="/windows/desktop/api/mprapi/ns-mprapi-auth_validation_ex">AUTH_VALIDATION_EX</a> structure.

### -field MPRAPI_OBJECT_TYPE_UPDATE_CONNECTION_OBJECT:5

The structure is a [RAS_UPDATE_CONNECTION](/windows/desktop/api/mprapi/ns-mprapi-ras_update_connection) structure.

### -field MPRAPI_OBJECT_TYPE_IF_CUSTOM_CONFIG_OBJECT:6

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mprapi_object_header">MPRAPI_OBJECT_HEADER</a>



<a href="/windows/desktop/RRAS/router-management-enumerations">Router Management Enumerated Types</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>
