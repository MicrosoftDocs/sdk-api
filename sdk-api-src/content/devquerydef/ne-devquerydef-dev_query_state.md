---
UID: NE:devquerydef._DEV_QUERY_STATE
tech.root: devinst
title: DEV_QUERY_STATE
ms.date: 10/31/2024
targetos: Windows
description: Specifies the state of the query associated with a DEV_QUERY_RESULT_ACTION_DATA structure.
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
 - _DEV_QUERY_STATE
 - PDEV_QUERY_STATE
 - DEV_QUERY_STATE
f1_keywords:
 - _DEV_QUERY_STATE
 - devquerydef/_DEV_QUERY_STATE
 - PDEV_QUERY_STATE
 - devquerydef/PDEV_QUERY_STATE
 - DEV_QUERY_STATE
 - devquerydef/DEV_QUERY_STATE
dev_langs:
 - c++
helpviewer_keywords:
 - _DEV_QUERY_STATE
---

## -description

Specifies the state of the query associated with a [DEV_QUERY_RESULT_ACTION_DATA](ns-devquerydef-dev_query_result_action_data.md) structure.

## -enum-fields

### -field DevQueryStateInitialized

The initial state of a query.

### -field DevQueryStateEnumCompleted

The initial enumeration of objects based on the current state of the system is complete. If [DevQueryFlagUpdateResults](ne-devquerydef-dev_query_flags.md) was specified during query creation, then further callbacks may happen as the state of the system changes. However, if **DevQueryFlagUpdateResults** was not specified during query creation, then this is the last callback, except for **DevQueryStateClosed** if [DevQueryFlagAsyncClose](e-devquerydef-dev_query_flags.md) was specified during query creation.

### -field DevQueryStateAborted

An out-of-resource error has occurred, and a notification could not be delivered. No further callbacks will occur. The client must close the query and create a new query to recover from this situation.

### -field DevQueryStateClosed

This state change only occurs when **DevQueryFlagAsyncClose** is specified during query creation. It indicates that closing the query has been completed. No further callbacks will occur.

## -remarks

## -see-also

