---
UID: NF:apiquery2.GetApiSetModuleBaseName
title: GetApiSetModuleBaseName function (apiquery2.h)
description: Retrieves the base name of the module that implements a specified API set, as recorded in the API set schema of the running system.
tech.root: winprog
ms.date: 09/03/2026
targetos: Windows
req.construct-type: function
req.header: apiquery2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: api-ms-win-core-apiquery-l2-1-1.dll
req.irql: 
req.typenames: 
req.redist: 
ms.custom: 19H1
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-core-apiquery-l2-1-1.dll
api_name:
 - GetApiSetModuleBaseName
f1_keywords:
 - GetApiSetModuleBaseName
 - apiquery2/GetApiSetModuleBaseName
dev_langs:
 - c++
helpviewer_keywords:
 - GetApiSetModuleBaseName
---

## -description

Retrieves the base name of the module that implements a specified [API set](/windows/win32/apiindex/windows-apisets), as recorded in the API set schema of the running system.

## -parameters

### -param contractName

The name of the API set to query. For the accepted forms, see the **Remarks** section.

The name can include a `.dll` suffix, as it appears in a PE Format import table, but the suffix isn't required. The function behaves the same with or without it.

### -param bufferLength

The capacity of the *moduleBaseName* buffer, in wide characters, including space for the null terminator.

Don't pass a capacity larger than 32,767 characters. A larger value is rejected with **E_NOT_SUFFICIENT_BUFFER** even when the name would otherwise fit. **MAX_PATH** is a suitable size, because the result is a file name rather than a path.

### -param moduleBaseName

A pointer to a caller-allocated buffer that receives the null-terminated host module base name.

This parameter is optional. To determine the required capacity without retrieving the name, pass **NULL** with *bufferLength* set to 0, and then read *actualNameLength* when the function returns **E_NOT_SUFFICIENT_BUFFER**.

When the function fails after its initial availability checks, a supplied buffer contains an empty string.

### -param actualNameLength

A pointer to a variable that receives the length of the host module base name, in wide characters, including the null terminator.

This parameter is optional and can be **NULL**.

The function writes this value on success, and also when it returns **E_NOT_SUFFICIENT_BUFFER**. A call that fails for insufficient capacity therefore reports the capacity that the buffer requires.

## -returns

Returns **S_OK** on success. Other possible values returned include the following.

|Return code|Description|
|-|-|
|HRESULT_FROM_NT(STATUS_INVALID_PARAMETER)|The API set contract name isn't well formed.|
|HRESULT_FROM_WIN32(ERROR_OBJECT_NOT_FOUND)|The schema query succeeded, but no host module is recorded for the API set contract name.|
|E_NOT_SUFFICIENT_BUFFER|*bufferLength* is too small for the name, or is larger than 32,767 characters. If *actualNameLength* is provided, the required length is written to that parameter.|
|E_POINTER|*moduleBaseName* is **NULL** even though *bufferLength* is large enough to receive the name.|

Additional failures from the underlying schema query are converted to an **HRESULT** and can propagate to the caller. Test the result with the **FAILED** macro rather than comparing it against a fixed set of values.

## -remarks

An [API set](/windows/win32/apiindex/windows-apisets) acts as an abstraction layer between the functional contract of a Win32 API and the module that implements it. That mapping can vary depending on the specific Windows product or enabled features. API set contract names might appear in a PE Format import table instead of a physical module name. The Windows loader resolves these names according to the API set schema composed for the running system.

**GetApiSetModuleBaseName** reports the host module base name that the schema records for a contract. It's especially useful for tools that analyze dependencies between Windows binaries, such as `.exe`, `.dll`, or `.sys` files, because it resolves API set contract names the same way the loader does.

The result is a schema lookup, not a file system operation. The function doesn't search the file system, confirm that the module exists on disk, load the module, or inspect its exports. A successful call reports the name that the running system's schema associates with the contract.

**GetApiSetModuleBaseName** is related to [IsApiSetImplemented](./nf-apiquery2-isapisetimplemented.md), which tests whether a contract is available without reporting the implementing module. The two functions consult the same schema but apply different resolution rules, so don't treat **HRESULT_FROM_WIN32(ERROR_OBJECT_NOT_FOUND)** as exactly equivalent to **IsApiSetImplemented** returning **FALSE**. Call the function whose result you actually need.

### Contract name forms

The *contractName* parameter uses the same contract-name vocabulary as **IsApiSetImplemented**.

| API surface | Name form | Example |
|---|---|---|
| Named group | `<contract>~<group>` | `api-win-core-samplefeature~AdvancedOperations` |
| Default group | Contract alias, without `~Default` | `api-win-core-samplefeature` |
| Versioned contract | Complete versioned contract name | `ext-ms-win-core-samplefeature-l1-1-0` |

The `samplefeature` names are illustrative names for a fictional Windows component. The contract prefix (`api-` or `ext-`) doesn't affect resolution behavior.

A `.dll` suffix is accepted but not required, which lets you pass a name taken directly from an import table.

### Buffer and length semantics

*bufferLength* and *actualNameLength* are both counts of wide characters, and both include the null terminator.

To retrieve a name in a single call, supply a buffer of **MAX_PATH** characters. To size the buffer first, make one call with *moduleBaseName* set to **NULL** and *bufferLength* set to 0, allocate the reported number of characters, and then call again.

### Availability and binding

This function is carried by the `api-ms-win-core-apiquery-l2-1-1` API set contract, which is a later version of the contract that carries **IsApiSetImplemented**. It isn't present on every system that provides *apiquery2.h*, and there's no import library that provides a downlevel-capable binding for it. Bind to it dynamically.

1. Call `IsApiSetImplemented("api-ms-win-core-apiquery-l2-1-1")`.
2. If the result is **TRUE**, call **LoadLibrary** on *api-ms-win-core-apiquery-l2-1-1.dll* and then **GetProcAddress** for `GetApiSetModuleBaseName`.
3. If the result is **FALSE**, use your fallback path and don't attempt the load.
4. Check the returned **HRESULT** and handle failure by taking the same fallback path as step 3.

The query in step 1 uses the conventional API set name without a `.dll` suffix. The loader call in step 2 uses the spelling found in an import table; either form works for that call.

**IsApiSetImplemented** is available through the OneCore umbrella libraries, so a program that uses this sequence still links an umbrella library for the query itself. For more info about that function and about umbrella library choice, see [IsApiSetImplemented](./nf-apiquery2-isapisetimplemented.md).

The declaration is available to the user-mode Desktop and System API partitions.

## Examples

The following example is a console app that prints the host module base name for an API set contract name passed as an argument. It binds to **GetApiSetModuleBaseName** dynamically, so it also runs on systems where the function isn't available.

```cpp
#include <windows.h>
#include <apiquery2.h>
#include <stdio.h>

typedef HRESULT (WINAPI *PFN_GET_API_SET_MODULE_BASE_NAME)(
    PCSTR   contractName,
    UINT32  bufferLength,
    PWSTR   moduleBaseName,
    UINT32* actualNameLength);

int __cdecl main(int argc, char* argv[])
{
    if (argc < 2)
    {
        wprintf(L"\nPlease supply an API set contract name\n\n");
        return 1;
    }

    PCSTR contractName = argv[1];

    // Test for the contract version that carries GetApiSetModuleBaseName.
    // Use the conventional API set name without the .dll suffix.
    if (!IsApiSetImplemented("api-ms-win-core-apiquery-l2-1-1"))
    {
        wprintf(L"GetApiSetModuleBaseName isn't available on this system.\n");
        return 1;
    }

    // The .dll suffix is optional here. It matches the spelling that
    // appears in an import table.
    HMODULE apiQuery = LoadLibraryExW(L"api-ms-win-core-apiquery-l2-1-1.dll",
                                      NULL,
                                      LOAD_LIBRARY_SEARCH_SYSTEM32);
    if (apiQuery == NULL)
    {
        wprintf(L"Couldn't load the API set: %u\n", GetLastError());
        return 1;
    }

    PFN_GET_API_SET_MODULE_BASE_NAME getApiSetModuleBaseName =
        (PFN_GET_API_SET_MODULE_BASE_NAME)GetProcAddress(apiQuery,
                                                         "GetApiSetModuleBaseName");
    if (getApiSetModuleBaseName == NULL)
    {
        wprintf(L"Couldn't resolve GetApiSetModuleBaseName: %u\n", GetLastError());
        FreeLibrary(apiQuery);
        return 1;
    }

    wchar_t baseName[MAX_PATH] = { 0 };
    UINT32 returnedLength = 0;

    HRESULT hr = getApiSetModuleBaseName(contractName,
                                         ARRAYSIZE(baseName),
                                         baseName,
                                         &returnedLength);
    if (FAILED(hr))
    {
        wprintf(L"GetApiSetModuleBaseName on %hs returns failure: 0x%08x\n",
                contractName, hr);
        FreeLibrary(apiQuery);
        return 2;
    }

    wprintf(L"API set %hs is implemented by %s\n", contractName, baseName);

    FreeLibrary(apiQuery);
    return 0;
}
```

## -see-also

* [Windows API sets](/windows/win32/apiindex/windows-apisets)

* [Detect API set availability](/windows/win32/apiindex/detect-api-set-availability)

* [IsApiSetImplemented](./nf-apiquery2-isapisetimplemented.md)
