---
UID: NF:apiquery2.GetApiSetModuleBaseName
title: GetApiSetModuleBaseName
description: Retrieves the file name of the module, or binary, that implements a specified API set.
tech.root: winprog
ms.date: 11/25/2025
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
req.lib: onecore.lib
req.dll: api-ms-win-core-apiquery-l2-1-0.dll
req.irql: 
req.typenames: 
req.redist: 
ms.custom: 19H1
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - api-ms-win-core-apiquery-l2
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

Retrieves the file name of the module, or binary, (such as a `.dll` or `.sys` file) that implements a specified [API set](/windows/win32/apiindex/windows-apisets).

## -parameters

### -param contractName

Specifies the name of the API set to query. For more info, see the **Remarks** section.

### -param bufferLength

The size of the buffer to receive the null-terminated string for the module file name, in characters. The maximum size of a host file name is **MAX_PATH**.

### -param moduleBaseName

A pointer to a string that receives the module file name.

### -param actualNameLength

The number of characters returned in the *moduleBaseName* buffer (including the null terminator).

## -returns

Returns S_OK on success. Other possible values returned include the following.

|Return code|Description|
|-|-|
|E_INVALIDARG|The API set contract name was not correctly formed.|
|HRESULT_FROM_WIN32(ERROR_OBJECT_NOT_FOUND)|The API set contract name was not found.|
|E_NOT_SUFFICIENT_BUFFER|The buffer length is insufficient for the host file name length. If actualNameLength is provided, the length required will be written to this parameter.|

## -remarks

An [API set](/windows/win32/apiindex/windows-apisets) acts as an abstraction layer between the functional contract of a Win32 API and the actual DLL that implements it. That mapping can vary depending on the specific Windows product or enabled features. API set contract names might appear in a PE Format import table instead of a physical module name. The Windows loader resolves these names according to the installed API set mapping.

The **GetApiSetModuleBaseName** function builds on the capabilities of [IsApiSetImplemented](./nf-apiquery2-isapisetimplemented.md). While **IsApiSetImplemented** checks whether a specific API contract is available, **GetApiSetModuleBaseName** retrieves the corresponding implementation file name if it exists.

If the API set contract isn't implemented, then **GetApiSetModuleBaseName** returns **HRESULT_FROM_WIN32(ERROR_OBJECT_NOT_FOUND)**. That's the same result as **IsApiSetImplemented** returning **FALSE**.

> [!NOTE]
> The API set contract name may include the `.dll` extension, as is common in a PE Format import table, but it's not required. The function will behave the same with or without a specified `.dll` extension. But the output *moduleFileName* will always include a file extension.

**GetApiSetModuleBaseName** is especially useful for tools that analyze dependencies between Windows binaries (such as `.exe`, `.dll`, or `.sys` files), as it allows them to resolve API set contract names to actual file names.

## Examples

The following example shows a simple console app that prints the API set module file name for a contract name passed as a parameter. The contract name must conform to the naming convention described in the *API set contract names* section in the [Windows API sets](/windows/win32/apiindex/windows-apisets) topic.

```cpp
#include <windows.h>
#include <stdio.h>
 
int __cdecl main(int argc, PCSTR argv[])
{
    if (argc < 2)
    {
        wprintf(L"\nPlease supply an API set contract name\n\n");
        return 1;
    }
 
    PCSTR apiSetContract = argv[1];
 
    wchar_t baseName[MAX_PATH] = { 0 };
    UINT32 returnedLength;
    HRESULT hr = GetApiSetModuleBaseName(apiSetContract, MAX_PATH, baseName, &returnedLength);
    if (FAILED(hr))
    {
        wprintf(L"GetApiSetModuleBaseName on %hs returns failure: 0x%x\n", apiSetContract, hr);
        return 2;
    }
 
    wprintf(L"API set %hs is implemented by %s\n", apiSetContract, hostName);
 
    return 0;
}
```

## -see-also

* [Windows API sets](/windows/win32/apiindex/windows-apisets)
