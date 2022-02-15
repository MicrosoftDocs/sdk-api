---
UID: NE:wdsclientapi.__unnamed_enum_1
title: __unnamed_enum_1 (wdsclientapi.h)
description: This enumeration is used by the WdsCliLog function.
helpviewer_keywords: ["WDS_LOG_TYPE_CLIENT","WDS_LOG_TYPE_CLIENT_APPLY_FINISHED","WDS_LOG_TYPE_CLIENT_APPLY_STARTED","WDS_LOG_TYPE_CLIENT_ERROR","WDS_LOG_TYPE_CLIENT_FINISHED","WDS_LOG_TYPE_CLIENT_GENERIC_MESSAGE","WDS_LOG_TYPE_CLIENT_IMAGE_SELECTED","WDS_LOG_TYPE_CLIENT_MAX_CODE","WDS_LOG_TYPE_CLIENT_STARTED","__unnamed_enum_1","enumeration [Windows Deployment Services]","wds.wds_log_type_client","wdsclientapi/","wdsclientapi/WDS_LOG_TYPE_CLIENT_APPLY_FINISHED","wdsclientapi/WDS_LOG_TYPE_CLIENT_APPLY_STARTED","wdsclientapi/WDS_LOG_TYPE_CLIENT_ERROR","wdsclientapi/WDS_LOG_TYPE_CLIENT_FINISHED","wdsclientapi/WDS_LOG_TYPE_CLIENT_GENERIC_MESSAGE","wdsclientapi/WDS_LOG_TYPE_CLIENT_IMAGE_SELECTED","wdsclientapi/WDS_LOG_TYPE_CLIENT_MAX_CODE","wdsclientapi/WDS_LOG_TYPE_CLIENT_STARTED"]
old-location: wds\wds_log_type_client.htm
tech.root: wds
ms.assetid: 6e49de64-28e4-41d6-a8cd-58348262b438
ms.date: 12/05/2018
ms.keywords: WDS_LOG_TYPE_CLIENT, WDS_LOG_TYPE_CLIENT_APPLY_FINISHED, WDS_LOG_TYPE_CLIENT_APPLY_STARTED, WDS_LOG_TYPE_CLIENT_ERROR, WDS_LOG_TYPE_CLIENT_FINISHED, WDS_LOG_TYPE_CLIENT_GENERIC_MESSAGE, WDS_LOG_TYPE_CLIENT_IMAGE_SELECTED, WDS_LOG_TYPE_CLIENT_MAX_CODE, WDS_LOG_TYPE_CLIENT_STARTED, __unnamed_enum_1, enumeration [Windows Deployment Services], wds.wds_log_type_client, wdsclientapi/, wdsclientapi/WDS_LOG_TYPE_CLIENT_APPLY_FINISHED, wdsclientapi/WDS_LOG_TYPE_CLIENT_APPLY_STARTED, wdsclientapi/WDS_LOG_TYPE_CLIENT_ERROR, wdsclientapi/WDS_LOG_TYPE_CLIENT_FINISHED, wdsclientapi/WDS_LOG_TYPE_CLIENT_GENERIC_MESSAGE, wdsclientapi/WDS_LOG_TYPE_CLIENT_IMAGE_SELECTED, wdsclientapi/WDS_LOG_TYPE_CLIENT_MAX_CODE, wdsclientapi/WDS_LOG_TYPE_CLIENT_STARTED
req.header: wdsclientapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __unnamed_enum_1
 - wdsclientapi/__unnamed_enum_1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wdsclientapi.h
api_name:
 - WDS_LOG_TYPE_CLIENT
---

# __unnamed_enum_1 enumeration


## -description

This enumeration is used by the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclilog">WdsCliLog</a> function.

## -enum-fields

### -field WDS_LOG_TYPE_CLIENT_ERROR:1

A client error message.

### -field WDS_LOG_TYPE_CLIENT_STARTED

A client started message.

### -field WDS_LOG_TYPE_CLIENT_FINISHED

A client finished message.

### -field WDS_LOG_TYPE_CLIENT_IMAGE_SELECTED

A client image selected message.

### -field WDS_LOG_TYPE_CLIENT_APPLY_STARTED

No additional parameters are required.

### -field WDS_LOG_TYPE_CLIENT_APPLY_FINISHED

No additional parameters are required.

### -field WDS_LOG_TYPE_CLIENT_GENERIC_MESSAGE

A generic message.

### -field WDS_LOG_TYPE_CLIENT_UNATTEND_MODE

### -field WDS_LOG_TYPE_CLIENT_TRANSFER_START

### -field WDS_LOG_TYPE_CLIENT_TRANSFER_END

### -field WDS_LOG_TYPE_CLIENT_TRANSFER_DOWNGRADE

### -field WDS_LOG_TYPE_CLIENT_DOMAINJOINERROR

### -field WDS_LOG_TYPE_CLIENT_POST_ACTIONS_START

### -field WDS_LOG_TYPE_CLIENT_POST_ACTIONS_END

### -field WDS_LOG_TYPE_CLIENT_APPLY_STARTED_2

### -field WDS_LOG_TYPE_CLIENT_APPLY_FINISHED_2

### -field WDS_LOG_TYPE_CLIENT_DOMAINJOINERROR_2

### -field WDS_LOG_TYPE_CLIENT_DRIVER_PACKAGE_NOT_ACCESSIBLE

### -field WDS_LOG_TYPE_CLIENT_OFFLINE_DRIVER_INJECTION_START

### -field WDS_LOG_TYPE_CLIENT_OFFLINE_DRIVER_INJECTION_END

### -field WDS_LOG_TYPE_CLIENT_OFFLINE_DRIVER_INJECTION_FAILURE

### -field WDS_LOG_TYPE_CLIENT_IMAGE_SELECTED2

### -field WDS_LOG_TYPE_CLIENT_IMAGE_SELECTED3

### -field WDS_LOG_TYPE_CLIENT_MAX_CODE

Used to determine an out-of-range index. Values greater than or equal to WDS_LOG_TYPE_CLIENT_MAX_CODE are not valid.
