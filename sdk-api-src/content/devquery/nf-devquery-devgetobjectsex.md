---
UID: NF:devquery.DevGetObjectsEx
tech.root: devinst
title: DevGetObjectsEx
ms.date: 11/06/2024
targetos: Windows
description: Synchronously retrieves a set of DEV_OBJECT structures based on the supplied requested properties, extended parameters, and filter criteria.
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
 - DevGetObjectsEx
f1_keywords:
 - DevGetObjectsEx
 - devquery/DevGetObjectsEx
dev_langs:
 - c++
helpviewer_keywords:
 - DevGetObjectsEx
---

## -description

Synchronously retrieves a set of [DEV_OBJECT](../devquerydef/ns-devquerydef-dev_object.md) structures based on the supplied requested properties, extended parameters, and filter criteria.

## -parameters

### -param ObjectType [in]

A value from the [DEV_OBJECT_TYPE](../devquerydef/ne-devquerydef-dev_object_type.md) enumeration that determines the object type that this query should operate on.

### -param QueryFlags [in]

A combination of [DEV_QUERY_FLAGS](../devquerydef/ne-devquerydef-dev_query_flags.md) values that are combined by using a bitwise OR operation. It is not valid to pass either **DevQueryFlagUpdateResults** or **DevQueryFlagAsyncClose** to this function.

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

### -param pcObjectCount [out]

The number of **DEV_OBJECT** structures returned in ppObjects.

### -param ppObjects [out]

Pointer that receives the newly allocated array of **DEV_OBJECT** results. Callers must free the pointer using [DevFreeObjects](nf-devquery-devfreeobjects.md). If no objects are enumerated, NULL will be returned.

## -returns

S_OK is returned if the function successfully evaluated the search criteria and returned matching objects; otherwise, an appropriate error value.

## -remarks

This function is an efficient way to synchronously enumerate objects while retrieving their properties. The array of objects that are returned must be freed using **DevFreeObjects**. If a requested property does not exist for an object that meets the filter criteria, then the **DEVPROPERTY** entry in the **DEV_OBJECT** for that property will have a type of [DEVPROP_TYPE_EMPTY](/windows-hardware/drivers/install/devprop-type-empty). 

Before using this function, consider how much data may be returned in the array and how long the call can block. It may be better to use the [DevCreateObjectQueryEx](nf-devquery-devcreateobjectqueryex.md) function, which allows the data to be consumed piecemeal and asynchronously.

The following example demonstrates the usage of **DevGetObjectsEx** to retrieve the set of **DEV_OBJECT** that matches a set of **DEVPROP_FILTER_EXPRESSION** structures.

```cpp
void
Example1()
{
    HRESULT hr = S_OK;
    ULONG ObjectCount = 0;
    const DEV_OBJECT* ObjectList = NULL;
    DEVPROP_BOOLEAN DevPropTrue = DEVPROP_TRUE;
    DEVPROPCOMPKEY RequestedProperties[] =
    {
        { DEVPKEY_Device_InstanceId, DEVPROP_STORE_SYSTEM, NULL }
    };
    DEVPROP_FILTER_EXPRESSION ObjectFilter[] =
    {
        {
            DEVPROP_OPERATOR_AND_OPEN, {0}
        },
        {
            DEVPROP_OPERATOR_EQUALS,
            {
                { DEVPKEY_DeviceInterface_Enabled, DEVPROP_STORE_SYSTEM, NULL },
                DEVPROP_TYPE_BOOLEAN,
                sizeof(DevPropTrue),
                (void*)&DevPropTrue
            }
        },
        {
            DEVPROP_OPERATOR_OR_OPEN, {0}
        },
        {
            DEVPROP_OPERATOR_EQUALS,
            {
                { DEVPKEY_DeviceInterface_ClassGuid, DEVPROP_STORE_SYSTEM, NULL },
                DEVPROP_TYPE_GUID,
                sizeof(GUID),
                (void*)&GUID_DEVINTERFACE_MOUSE
            }
        },
        {
            DEVPROP_OPERATOR_EQUALS,
            {
                { DEVPKEY_DeviceInterface_ClassGuid, DEVPROP_STORE_SYSTEM, NULL },
                DEVPROP_TYPE_GUID,
                sizeof(GUID),
                (void*)&GUID_DEVINTERFACE_KEYBOARD
            }
        },
        {
            DEVPROP_OPERATOR_OR_CLOSE, {0}
        },
        {
            DEVPROP_OPERATOR_AND_CLOSE, {0}
        }
    };

    hr = DevGetObjectsEx(DevObjectTypeDeviceInterface,
                         DevQueryFlagNone,
                         RTL_NUMBER_OF(RequestedProperties),
                         RequestedProperties,
                         RTL_NUMBER_OF(ObjectFilter),
                         ObjectFilter,
                         0,
                         NULL,
                         &ObjectCount,
                         &ObjectList);

    if (FAILED(hr))
    {
        wprintf(L"Failed to retrieve objects. hr = 0x%08x\n", hr);
        goto exit;
    }

    for (ULONG i = 0; i < ObjectCount; i++)
    {
        wprintf(L"Retrieved object '%ws'\n",
                ObjectList[i].pszObjectId);
    }

  exit:

    if (ObjectList != NULL)
    {
        DevFreeObjects(ObjectCount, ObjectList);
    }

    return;
}
```

## -see-also

[DevCreateObjectQuery](nf-devquery-devcreateobjectquery.md)

