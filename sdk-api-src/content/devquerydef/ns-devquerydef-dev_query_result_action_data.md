---
UID: NS:devquerydef._DEV_QUERY_RESULT_ACTION_DATA
tech.root: devinst
title: DEV_QUERY_RESULT_ACTION_DATA
ms.date: 10/31/2024
targetos: Windows
description: Provides information to the PDEV_QUERY_RESULT_CALLBACK callback function.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: devquerydef.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: DEV_QUERY_RESULT_ACTION_DATA, *PDEV_QUERY_RESULT_ACTION_DATA
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - devquerydef.h
api_name:
 - _DEV_QUERY_RESULT_ACTION_DATA
 - PDEV_QUERY_RESULT_ACTION_DATA
 - DEV_QUERY_RESULT_ACTION_DATA
f1_keywords:
 - _DEV_QUERY_RESULT_ACTION_DATA
 - devquerydef/_DEV_QUERY_RESULT_ACTION_DATA
 - PDEV_QUERY_RESULT_ACTION_DATA
 - devquerydef/PDEV_QUERY_RESULT_ACTION_DATA
 - DEV_QUERY_RESULT_ACTION_DATA
 - devquerydef/DEV_QUERY_RESULT_ACTION_DATA
dev_langs:
 - c++
helpviewer_keywords:
 - _DEV_QUERY_RESULT_ACTION_DATA
---

## -syntax

```cpp
typedef struct _DEV_QUERY_RESULT_ACTION_DATA {
  DEV_QUERY_RESULT_ACTION          Action;
  union _DEV_QUERY_RESULT_UPDATE_PAYLOAD {
    DEV_QUERY_STATE State;
    DEV_OBJECT      DeviceObject;
  } Data;
} DEV_QUERY_RESULT_ACTION_DATA, *PDEV_QUERY_RESULT_ACTION_DATA;
```

## -description

Provides information to the [PDEV_QUERY_RESULT_CALLBACK](../devquery/nc-devquery-pdev_query_result_callback.md) callback function.

## -struct-fields

### -field Action

A value from the [DEV_QUERY_RESULT_ACTION](ne-devquerydef-dev_query_result_action.md) enumeration specifying the type of action being performed.

### -field Data

A value from the *_DEV_QUERY_RESULT_UPDATE_PAYLOAD* union.

### -field Data.State

A value from the [DEV_QUERY_STATE](ne-devquerydef-dev_query_state.md) enumeration specifying the current state of the query. This member is valid only if *Action* is equal to [DevQueryResultStateChange](ne-devquerydef-dev_query_result_action.md).

### -field Data.DeviceObject

A [DEV_OBJECT](ns-devquerydef-dev_object.md) structure associated with the query result. This member is only valid if *Action* is equal to **DevQueryResultAdd**, **DevQueryResultUpdate**, or **DevQueryResultRemove**. The following table specifies how the *DevObject* field should be interpreted, depending on the value of the *Action* field.

| Action value | Interpretation of *DeviceObject* |
|--------------|------------------------------|
| **DevQueryResultAdd** | *DeviceObject* represents a new object being added to the query’s result set due to it meeting the criteria of the query’s filter parameters. *DeviceObject* will contain a list of properties for all properties requested by the query. |
| **DevQueryResultUpdate** | *DeviceObject* represents an object already in the query’s result set that has had a requested property changed. The property list in *DeviceObject* will provide the properties that have changed. |
| **DevQueryResultRemove** | *DeviceObject* represents an object that is being removed from the query’s result set due to it no longer meeting the criteria of the query’s filter parameters. |

### -field _DEV_QUERY_RESULT_UPDATE_PAYLOAD

The union containing the the state or object associated with the action.

## -remarks

## -see-also

