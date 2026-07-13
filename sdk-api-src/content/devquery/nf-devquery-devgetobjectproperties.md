---
UID: NF:devquery.DevGetObjectProperties
tech.root: devinst
title: DevGetObjectProperties
ms.date: 11/06/2024
targetos: Windows
description: Synchronously retrieve a set of properties for a specified object.
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
 - api-ms-win-devices-query-l1-1-0.dll
 - Cfgmgr32.dll
api_name:
 - DevGetObjectProperties
f1_keywords:
 - DevGetObjectProperties
 - devquery/DevGetObjectProperties
dev_langs:
 - c++
helpviewer_keywords:
 - DevGetObjectProperties
---

## -description

Synchronously retrieve a set of properties for a specified object

## -parameters

### -param ObjectType [in]

A value from the [DEV_OBJECT_TYPE](../devquerydef/ne-devquerydef-dev_object_type.md) that determines the type of object for which properties are to be retrieved.

### -param pszObjectId [in]

The identity of the object for which properties are to be retrieved.

### -param QueryFlags [in]

A combination of [DEV_QUERY_FLAGS](../devquerydef/ne-devquerydef-dev_query_flags.md) values that are combined by using a bitwise OR operation. It is not valid to pass either **DevQueryFlagUpdateResults** or **DevQueryFlagAsyncClose** to this function.

### -param cRequestedProperties [in]

The number of [DEVPROPCOMPKEY](/windows-hardware/drivers/install/devpropcompkey) structures provided in *pRequestedProperties*. If [DevQueryFlagAllProperties](../devquerydef/ne-devquerydef-dev_query_flags.md) is specified, this must be set to 0.

### -param pRequestedProperties [in]

Provides an array of **DEVPROPCOMPKEY** structures that specify the properties that should be retrieved for the specified object.

The *LocaleName* field of the **DEVPROPCOMPKEY** structure is ignored and must be set to NULL.

If *cRequestedProperties* is 0, this must be NULL.

### -param pcPropertyCount [out]

The number of [DEVPROPERTY](/windows-hardware/drivers/install/devproperty) structures returned in *ppProperties*.

### -param ppProperties [out]

Pointer that receives the newly allocated array of **DEVPROPERTY** results. Callers must free the pointer using [DevFreeObjectProperties](nf-devquery-devfreeobjectproperties.md).

## -returns

S_OK is returned if the function successfully evaluated the search criteria and returned matching objects; otherwise, an appropriate error value.

## -remarks

This function is an efficient way to synchronously retrieve a set of properties from an object given its type and identity. The array of properties that are returned must be freed using **DevFreeObjectProperties**. If a requested property does not exist, *ppProperties* will still contain an entry for that property but the entry will have a type of [DEVPROP_TYPE_EMPTY](/windows-hardware/drivers/install/devprop-type-empty).

## Example

The following example demonstrates calling **DevGetObjectProperties** to retrieve a set of requested properties and then calling [DevFindProperty](nf-devquery-devfindproperty.md) to find a particular property within an array of **DEVPROPERTY** structures.

```cpp
void
Example1(PCWSTR DeviceInstancePath)
{
    HRESULT hr = S_OK;
    const DEVPROPERTY* TempProperty = NULL;
    ULONG PropertyCount = 0;
    const DEVPROPERTY* PropertyList = NULL;
    DEVPROPCOMPKEY RequestedProperties[] =
    {
        { DEVPKEY_Device_HardwareIds, DEVPROP_STORE_SYSTEM, NULL },
        { DEVPKEY_Device_CompatibleIds, DEVPROP_STORE_SYSTEM, NULL }
    };

    hr = DevGetObjectProperties(DevObjectTypeDevice,
                                DeviceInstancePath,
                                DevQueryFlagNone,
                                RTL_NUMBER_OF(RequestedProperties),
                                RequestedProperties,
                                &PropertyCount,
                                &PropertyList);

    if (FAILED(hr))
    {
        wprintf(L"Failed to retrieve properties. hr = 0x%08x\n", hr);
        goto exit;
    }

    wprintf(L"Hardware IDs:\n");
    TempProperty = DevFindProperty(&DEVPKEY_Device_HardwareIds,
                                   DEVPROP_STORE_SYSTEM,
                                   NULL,
                                   PropertyCount,
                                   PropertyList);

    if ((TempProperty == NULL) ||
        (TempProperty->Type == DEVPROP_TYPE_EMPTY) ||
        (TempProperty->Buffer == NULL))
    {
        wprintf(L"<none>\n");
    }
    else if ((TempProperty->Type != DEVPROP_TYPE_STRING_LIST) ||
             (TempProperty->BufferSize < sizeof(WCHAR)))
    {
        wprintf(L"Device '%ws' has a corrupted Hardware IDs property.\n",
                DeviceInstancePath);
    }
    else
    {
        for (PCWSTR CurrentId = (PCWSTR)TempProperty->Buffer;
             *CurrentId != L'\0';
             CurrentId += wcslen(CurrentId) + 1)
        {
            wprintf(L"%ws\n", CurrentId);
        }
    }

    wprintf(L"\nCompatible IDs:\n");
    TempProperty = DevFindProperty(&DEVPKEY_Device_CompatibleIds,
                                   DEVPROP_STORE_SYSTEM,
                                   NULL,
                                   PropertyCount,
                                   PropertyList);

    if ((TempProperty == NULL) ||
        (TempProperty->Type == DEVPROP_TYPE_EMPTY) ||
        (TempProperty->Buffer == NULL))
    {
        wprintf(L"<none>\n");
    }
    else if ((TempProperty->Type != DEVPROP_TYPE_STRING_LIST) ||
             (TempProperty->BufferSize < sizeof(WCHAR)))
    {
        wprintf(L"Device '%ws' has a corrupted Compatible IDs property.\n",
                DeviceInstancePath);
    }
    else
    {
        for (PCWSTR CurrentId = (PCWSTR)TempProperty->Buffer;
             *CurrentId != L'\0';
             CurrentId += wcslen(CurrentId) + 1)
        {
            wprintf(L"%ws\n", CurrentId);
        }
    }

  exit:

    if (PropertyList != NULL)
    {
        DevFreeObjectProperties(PropertyCount, PropertyList);
    }

    return;
}
```

## -see-also

