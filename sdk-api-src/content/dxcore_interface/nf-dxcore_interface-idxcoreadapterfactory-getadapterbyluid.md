---
UID: NF:dxcore_interface.IDXCoreAdapterFactory.GetAdapterByLuid
title: IDXCoreAdapterFactory::GetAdapterByLuid
description: Retrieves the DXCore adapter object ([IDXCoreAdapter](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapter)) for a specified LUID, if available.
author: windows-sdk-content
tech.root: dxcore
ms.author: windowssdkdev
ms.date: 06/10/2019
ms.keywords: IDXCoreAdapterFactory interface,GetAdapterByLuid method, IDXCoreAdapterFactory.GetAdapterByLuid, IDXCoreAdapterFactory::GetAdapterByLuid, GetAdapterByLuid, GetAdapterByLuid method, GetAdapterByLuid method,IDXCoreAdapterFactory interface, dxcore/IDXCoreAdapterFactory::GetAdapterByLuid, dxcore_interface.idxcoreadapterfactory_getadapterbyluid
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
 - IDXCoreAdapterFactory.GetAdapterByLuid
---

## -description

Retrieves the DXCore adapter object ([IDXCoreAdapter](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapter)) for a specified LUID, if available. For programming guidance, and code examples, see [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters).

## -parameters

### -param adapterLUID

Type: **[LUID](/windows/win32/api/winnt/ns-winnt-_luid) const\&**

The locally unique value that identifies the adapter instance.

### -param riid [in]

Type: **REFIID**

A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapter*. This is expected to be the interface identifier (IID) of [IDXCoreAdapter](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapter).

### -param ppvAdapter [out]

Type: **void\*\***

The address of a pointer to an interface with the IID specified in the *riid* parameter. Upon successful return, *\*ppvAdapter* (the dereferenced address) contains a pointer to the the DXCore adapter created.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|The adapter LUID passed in *adapterLUID* is recognized, but the adapter is no longer in a valid state.|
|E_INVALIDARG|No such adapter LUID as the value passed in *adapterLUID* is available through DXCore.|
|E_NOINTERFACE|An invalid value was provided for *riid*.|
|E_POINTER|`nullptr` was provided for *ppvAdapter*.|

## -remarks

Multiple calls passing the same [LUID](/windows/win32/api/winnt/ns-winnt-_luid) return identical interface pointers. As a result, it's safe to compare interface pointers to determine whether multiple pointers refer to the same adapter object.

## -see-also

[IDXCoreAdapterFactory](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory), [DXCore Reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
