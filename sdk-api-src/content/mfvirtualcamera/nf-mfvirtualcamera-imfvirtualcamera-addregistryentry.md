---
UID: NF:mfvirtualcamera.IMFVirtualCamera.AddRegistryEntry
tech.root: mf
title: IMFVirtualCamera::AddRegistryEntry
ms.date: 05/17/2021
targetos: Windows
description: Adds a custom registry entry to the device interface registry key.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: mfsensorgroup.dll
req.header: mfvirtualcamera.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: mfsensorgroup.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - mfsensorgroup.dll
api_name:
 - IMFVirtualCamera::AddRegistryEntry
f1_keywords:
 - IMFVirtualCamera::AddRegistryEntry
 - mfvirtualcamera/IMFVirtualCamera::AddRegistryEntry
dev_langs:
 - c++
---

## -description

Adds a custom registry entry to the device interface registry key.

## -parameters

### -param EntryName

A null-terminated Unicode string representing the registry entry name.

### -param SubkeyPath

Optional null-terminated Unicode string representing a subkey under the device interface registry node.

### -param dwRegType

The data type of the registry entry. The **REG_NONE** type is not supported. For more information, see [Registry Value Types](/windows/win32/sysinfo/registry-value-types).

### -param pbData

Pointer to the data for the registry entry.

### -param cbData

Size of the data in the buffer pointed to by *pbData*, in bytes.

## -returns

Returns an HRESULT value, including but not limited to the following values:

| Error code | Description |
|------------|-------------|
| S_OK    | Succeeded |
| E_INVALIDARG | An input parameter is invalid. |
| E_ACCESSDENIED | Caller has insufficient permissions to add properties. |

## -remarks

Callers must have administrator-level permissions to use this API. UWP and packaged apps do not have permissions to call this method.

## -see-also

