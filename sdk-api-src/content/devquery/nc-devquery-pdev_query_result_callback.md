---
UID: NC:devquery.PDEV_QUERY_RESULT_CALLBACK
tech.root: devinst
title: PDEV_QUERY_RESULT_CALLBACK
ms.date: 10/31/2024
targetos: Windows
description: The function prototype required of callback functions that will receive DevQuery query results.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: devquery.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - devquery.h
api_name:
 - PDEV_QUERY_RESULT_CALLBACK
f1_keywords:
 - PDEV_QUERY_RESULT_CALLBACK
 - devquery/PDEV_QUERY_RESULT_CALLBACK
dev_langs:
 - c++
helpviewer_keywords:
 - PDEV_QUERY_RESULT_CALLBACK
---

## -description

The function prototype required of callback functions that will receive DevQuery query results.

## -parameters

### -param hDevQuery

Handle for the query associated with the callback.

### -param pContext

The optional context value provided by the client during query creation.

### -param pActionData

A [DEV_QUERY_RESULT_ACTION_DATA](../devquerydef/ns-devquerydef-dev_query_result_action_data.md) structure that provides information about the change to the query state or the action applied to the result set. The data in this structure will be freed once the callback returns.

## -remarks

Only one callback function is ever active for a given query. If the same callback function is passed to multiple queries, it is possible for the callback functions to execute concurrently, because they can be invoked for different queries.

You can only call [DevCloseObjectQuery](nf-devquery-devcloseobjectquery.md) on the *hDevQuery* handle from the callback if the [DevQueryFlagAsyncClose](../devquerydef/ne-devquerydef-dev_query_flags.md) flag was specified when the query was created. If **DevQueryFlagAsyncClose** was not specified, calling **DevCloseObjectQuery** on a query from inside its own callback will result in a deadlock.


## -see-also

