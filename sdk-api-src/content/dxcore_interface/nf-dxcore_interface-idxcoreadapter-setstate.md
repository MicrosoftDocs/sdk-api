---
UID: NF:dxcore_interface.IDXCoreAdapter.SetState
title: IDXCoreAdapter::SetState
description: Sets the state of the specified item on the adapter.
tech.root: dxcore
ms.date: 06/10/2019
ms.keywords: IDXCoreAdapter interface,SetState method, IDXCoreAdapter.SetState, IDXCoreAdapter::SetState, SetState, SetState method, SetState method,IDXCoreAdapter interface, dxcore/IDXCoreAdapter::SetState, dxcore_interface.idxcoreadapterfactory_setstate
ms.localizationpriority: low
targetos: Windows
product: Windows
req.assembly: 
req.construct-type: method
req.ddi-compliance: 
req.dll: dxcore.dll
req.header: dxcore_interface.h
req.idl: 
req.include-header: dxcore.h
req.irql: 
req.kmdf-ver: 
req.lib: dxcore.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 (Build 18936)
req.target-min-winversvr: 
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
 - kbsyntax
api_type:
 - COM
api_location:
 - dxcore.dll
api_name:
 - IDXCoreAdapter::SetState
---

## -description

Sets the state of the specified item on the adapter. Before calling **SetState** for a property type, call [IsSetStateSupported](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-issetstatesupported) to confirm that setting the state kind is available for this adapter and operating system (OS).

## -parameters

### -param state

Type: **[DXCoreAdapterState](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcoreadapterstate)**

The kind of state item on the adapter whose state you wish to set. See the table in [DXCoreAdapterState](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcoreadapterstate) for more info about each adapter state kind.

### -param inputStateDetailsSize

Type: **size_t**

The size, in bytes, of the input state details buffer that you (optionally) allocate and provide in *inputStateDetails*.

### -param inputStateDetails [in]

Type: **void const\***

An optional pointer to a constant input state details buffer that you allocate in your application, containing any information about your request that's required for the state kind you specify in *state*. See the table in [DXCoreAdapterState](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcoreadapterstate) for more info about any input buffer requirement for a given state kind.

### -param inputDataSize

Type: **size_t**

The size, in bytes, of the input buffer that you allocate and provide in *inputData*.

### -param inputData [in]

Type: **void\***

A pointer to an input buffer that you allocate in your application, containing the state information to set for the state item whose kind you specify in *state*. See the table in [DXCoreAdapterState](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcoreadapterstate) for more info about the input buffer requirement for a given state kind.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|The adapter is no longer in a valid state.|
|DXGI_ERROR_INVALID_CALL|The state kind specified in *state* is not recognized by this operating system (OS). Call [IsSetStateSupported](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-issetstatesupported) to confirm that setting the state kind is available for this adapter and operating system (OS).|
|DXGI_ERROR_UNSUPPORTED|The state kind specified in *state* is not supported by the adapter. Call [IsSetStateSupported](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-issetstatesupported) to confirm that setting the state kind is available for this adapter and operating system (OS).|
|E_INVALIDARG|An insufficient buffer size is provided for *inputData* (or for *inputStateDetails* where an input state details buffer is necessary).|
|E_POINTER|`nullptr` was provided for *inputData* (or for *inputStateDetails* where an input state details buffer is necessary).|

## -see-also

[IDXCoreAdapter](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapter), [DXCore Reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
