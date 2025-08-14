---
UID: NF:devquery.DevCreateObjectQueryFromIdsEx
tech.root: devinst
title: DevCreateObjectQueryFromIdsEx
ms.date: 11/06/2024
targetos: Windows
description: Creates a device query to retrieve properties based on the specified query parameters, extended parameters, and a list of object IDs.
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
 - DevCreateObjectQueryFromIdsEx
f1_keywords:
 - DevCreateObjectQueryFromIdsEx
 - devquery/DevCreateObjectQueryFromIdsEx
dev_langs:
 - c++
helpviewer_keywords:
 - DevCreateObjectQueryFromIdsEx
---

## -description

Creates a device query to retrieve properties based on the specified query parameters, extended parameters, and a list of object IDs.

## -parameters

### -param ObjectType [in]

A value from the [DEV_OBJECT_TYPE](../devquerydef/ne-devquerydef-dev_object_type.md) enumeration that determines the object type that this query should operate on.

### -param pszzObjectIds [in]

A multi-sz list of object identifiers for objects the query should operate on. For information about multi-sz strings, see [REG_MULTI_SZ](/windows/win32/sysinfo/registry-value-types).

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

A [PDEV_QUERY_RESULT_CALLBACK](nc-devquery-pdev_query_result_callback.md) callback function that results for this query should be sent to

### -param pContext [in, optional]

Caller-supplied context. This value is passed to the callback function unmodified.

### -param phDevQuery [out]

Pointer that receives the handle representing the query. If **DevQueryFlagsUpdateResults** is specified, then the query will receive
updates until the handle is closed. Call [DevCloseObjectQuery](nf-devquery-devcloseobjectquery.md) to close this handle to stop the query.

## -returns

S_OK is returned if a query was successfully created; otherwise, an appropriate error value.

## -remarks

For an example of creating device query to retrieve properties based on the specified query parameters and a list of object IDs, see [DevCreateObjectQueryFromIds](nf-devquery-devcreateobjectqueryfromids.md).

## -see-also

[DevCreateObjectQuery](nf-devquery-devcreateobjectquery.md)

