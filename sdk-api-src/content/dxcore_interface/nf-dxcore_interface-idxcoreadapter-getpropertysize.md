---
UID: NF:dxcore_interface.IDXCoreAdapter.GetPropertySize
title: IDXCoreAdapter::GetPropertySize
description: For a specified adapter property, retrieves the size of buffer, in bytes, that is required for a call to [GetProperty](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty).
author: windows-sdk-content
tech.root: dxcore
ms.author: windowssdkdev
ms.date: 06/10/2019
ms.keywords: IDXCoreAdapter interface,GetPropertySize method, IDXCoreAdapter.GetPropertySize, IDXCoreAdapter::GetPropertySize, GetPropertySize, GetPropertySize method, GetPropertySize method,IDXCoreAdapter interface, dxcore/IDXCoreAdapter::GetPropertySize, dxcore_interface.idxcoreadapterfactory_getpropertysize
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
 - IDXCoreAdapter::GetPropertySize
---

## -description

For a specified adapter property, retrieves the size of buffer, in bytes, that is required for a call to [GetProperty](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty). Before calling **GetPropertySize** for a property type, call [IsPropertySupported](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported) to confirm that the property type is available for this adapter and operating system (OS).

## -parameters

### -param property

Type: **[DXCoreAdapterProperty](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty)**

The type of the property whose size, in bytes, you wish to retrieve.

### -param bufferSize [out]

Type: **size_t\***

A pointer to a **size_t** value. The function dereferences the pointer and sets the value to the size, in bytes, of the output buffer that you should allocate and pass as the *propertyData* argument in your call to [GetProperty](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty).

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|DXGI_ERROR_INVALID_CALL|The property type specified in *property* is not recognized by this operating system (OS). Call [IsPropertySupported](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported) to confirm that the property type is available for this adapter and operating system (OS).|
|DXGI_ERROR_UNSUPPORTED|The property type specified in *property* is not supported by the adapter. Call [IsPropertySupported](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported) to confirm that the property type is available for this adapter and operating system (OS).|
|E_POINTER|`nullptr` was provided for *bufferSize*.|

## -remarks

You can call **GetPropertySize** on an adapter that's no longer valid&mdash;the function won't fail.

## -see-also

[IDXCoreAdapter](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapter), [DXCore Reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
