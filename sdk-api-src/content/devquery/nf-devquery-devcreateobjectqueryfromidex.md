---
UID: NF:devquery.DevCreateObjectQueryFromIdEx
tech.root: devinst
title: DevCreateObjectQueryFromIdEx
ms.date: 11/05/2024
targetos: Windows
description: Creates a device query to retrieve properties based on the specified query parameters, extended parameters, and object ID.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Cfgmgr32.dll
req.header: devquery.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Onecore.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 version 1809
req.target-min-winversvr: Windows Server 2019
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-devices-query-l1-1-1.dll
 - Cfgmgr32.dll
api_name:
 - DevCreateObjectQueryFromIdEx
f1_keywords:
 - DevCreateObjectQueryFromIdEx
 - devquery/DevCreateObjectQueryFromIdEx
dev_langs:
 - c++
helpviewer_keywords:
 - DevCreateObjectQueryFromIdEx
---

## -description

Creates a device query to retrieve properties based on the specified query parameters, extended parameters, and object ID.

## -parameters

### -param ObjectType [in]

A value from the [DEV_OBJECT_TYPE](../devquerydef/ne-devquerydef-dev_object_type.md) enumeration that determines the object type that this query should operate on.


### -param pszObjectId [in]

The string identifier for the specific object the query should operate on.

### -param QueryFlags [in]

A combination of [DEV_QUERY_FLAGS](../devquerydef/ne-devquerydef-dev_query_flags.md) values that are combined by using a bitwise OR operation.

### -param cRequestedProperties [in]

The number of [DEVPROPCOMPKEY](/windows-hardware/drivers/install/devpropcompkey) structures provided in *pRequestedProperties*. If [DevQueryFlagAllProperties](../devquerydef/ne-devquerydef-dev_query_flags.md) is specified, this must be set to 0.

### -param pRequestedProperties [in, optional]

Optionally provides an array of **DEVPROPCOMPKEY** structures that specify the properties that should be retrieved for objects in the
query’s result set when *pCallback* is called to notify the query of an addition of an object to its result set.  
If [DevQueryFlagUpdateResults](../devquerydef/ne-devquerydef-dev_query_flags.md) was specified in *QueryFlags*, the query will be notified
if the value of any of these properties changes for any object in the query’s result set.

The *LocaleName* field of the **DEVPROPCOMPKEY** structure is ignored and must be set to NULL.

If *cRequestedProperties* is 0, this must be NULL.

### -param cFilterExpressionCount [in]

The number of [DEVPROP_FILTER_EXPRESSION](../devfiltertypes/ns-devfiltertypes-devprop_filter_expression.md) structures provided in *pFilter*.

### -param pFilter [in, optional]

Optionally provides an array of **DEVPROP_FILTER_EXPRESSION** structures that specify filter criteria for what objects should be part
of the query’s result set. If *cFilterExpressionCount* is 0, this must be NULL.

### -param cExtendedParameterCount [in]

Reserved for system usage. Must be set to 0.

### -param pExtendedParameters [in, optional]

Reserved for system usage. Must be set to NULL.

### -param pCallback [in]

A [PDEV_QUERY_RESULT_CALLBACK](nc-devquery-pdev_query_result_callback.md) callback function that results for this query should be sent to.

### -param pContext [in, optional]

Caller-supplied context. This value is passed to the callback function unmodified.

### -param phDevQuery [out]

Pointer that receives the handle representing the query. If **DevQueryFlagsUpdateResults** is specified, then the query will receive
updates until the handle is closed. Call [DevCloseObjectQuery](nf-devquery-devcloseobjectquery.md) to close this handle to stop the query.

## -returns

S_OK is returned if a query was successfully created; otherwise, an appropriate error value.

## -remarks

When a client wants to retrieve data about a specific object given its identity, use this function rather than [DevCreateObjectQuery](nf-devquery-devcreateobjectquery.md) with a filter. This function is more efficient.

For more information, see the remarks section of [DevCreateObjectQuery](nf-devquery-devcreateobjectquery.md), which also
apply to this function. For an example of creating a device query to retrieve properties based on the specified query parameters and object ID, see [DevCreateObjectQueryFromId](nf-devquery-devcreateobjectqueryfromid.md).

## -see-also

[DevCreateObjectQuery](nf-devquery-devcreateobjectquery.md)

