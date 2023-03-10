---
UID: NF:mmdeviceapi.IAudioSystemEffectsPropertyStore.OpenVolatilePropertyStore
tech.root: audio
title: IAudioSystemEffectsPropertyStore::OpenVolatilePropertyStore
ms.date: 06/18/2021
targetos: Windows
description: Opens the audio system effects volatile property store.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mmdeviceapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
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
 - COM
api_location:
 - mmdeviceapi.h
api_name:
 - IAudioSystemEffectsPropertyStore::OpenVolatilePropertyStore
f1_keywords:
 - IAudioSystemEffectsPropertyStore::OpenVolatilePropertyStore
 - mmdeviceapi/IAudioSystemEffectsPropertyStore::OpenVolatilePropertyStore
dev_langs:
 - c++
---

## -description

Opens the audio system effects volatile property store.

## -parameters

### -param stgmAccess

The storage-access mode. This parameter specifies whether to open the property store in read mode, write mode, or read/write mode. Set this parameter to one of the following STGM constants:

STGM_READ

STGM_WRITE

STGM_READWRITE

The method permits a client running as an administrator to open a store for read-only, write-only, or read/write access. A client that is not running as an administrator is restricted to read-only access.

### -param propStore

Receives a pointer to an [IPropertyStore](../propsys/nn-propsys-ipropertystore.md) representing the volatile property store.

## -returns

Returns an HRESULT including, but not limited to the following:

| Value | Description |
|-------|-------------|
| S_OK  | Success     |
| E_NOTFOUND | The call is attempting to open a property store that does not exist. See Remarks. |
| E_ACCESSDENIED | The caller was denied access for the specified *stgmAccess* value |

## -remarks

This method will only open existing property stores under the context registry keys. It will not create a new key if one is not present in the associated INF file. Attempting to access a property store that does not already exist will result in an E_NOTFOUND error.

For more information on the Windows 11 APIs for the Audio Processing Objects (APOs) that can ship with audio drivers, see [Windows 11 APIs for Audio Processing Objects](/windows-hardware/drivers/audio/windows-11-apis-for-audio-processing-objects).

## -see-also

