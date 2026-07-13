---
UID: NE:devquerydef._DEV_QUERY_RESULT_ACTION
tech.root: devinst
title: DEV_QUERY_RESULT_ACTION
ms.date: 10/31/2024
targetos: Windows
description: Specifies the type of action associated with a DEV_QUERY_RESULT_ACTION_DATA structure.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: devquerydef.h
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
 - devquerydef.h
api_name:
 - _DEV_QUERY_RESULT_ACTION
 - PDEV_QUERY_RESULT_ACTION
 - DEV_QUERY_RESULT_ACTION
f1_keywords:
 - _DEV_QUERY_RESULT_ACTION
 - devquerydef/_DEV_QUERY_RESULT_ACTION
 - PDEV_QUERY_RESULT_ACTION
 - devquerydef/PDEV_QUERY_RESULT_ACTION
 - DEV_QUERY_RESULT_ACTION
 - devquerydef/DEV_QUERY_RESULT_ACTION
dev_langs:
 - c++
helpviewer_keywords:
 - _DEV_QUERY_RESULT_ACTION
---

## -description

Specifies the type of action associated with a [DEV_QUERY_RESULT_ACTION_DATA](ns-devquerydef-dev_query_result_action_data.md) structure.

## -enum-fields

### -field DevQueryResultStateChange

The state of the query has changed. The *State* member of the **DEV_QUERY_RESULT_ACTION_DATA** structure contains the new state.

### -field DevQueryResultAdd

The object specified in *DeviceObject* member of the **DEV_QUERY_RESULT_ACTION_DATA** structure has been added to the client's result-set.

### -field DevQueryResultUpdate

The object specified in *DeviceObject* member of the **DEV_QUERY_RESULT_ACTION_DATA** structure has changed.

### -field DevQueryResultRemove

The object specified in *DeviceObject* member of the **DEV_QUERY_RESULT_ACTION_DATA** structure has been removed from the client's result-set.

## -remarks

## -see-also

