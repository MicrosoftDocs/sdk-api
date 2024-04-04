---
UID: NF:dxcore_interface.IDXCoreAdapterList.GetFactory
title: IDXCoreAdapterList::GetFactory
description: Retrieves an IDXCoreAdapterFactory interface pointer to the DXCore adapter factory object.
tech.root: dxcore
ms.date: 06/10/2019
ms.keywords: IDXCoreAdapterFactory interface,GetFactory method, IDXCoreAdapterFactory.GetFactory, IDXCoreAdapterFactory::GetFactory, GetFactory, GetFactory method, GetFactory method,IDXCoreAdapterFactory interface, dxcore/IDXCoreAdapterFactory::GetFactory, dxcore_interface.idxcoreadapterfactory_getfactory
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
 - IDXCoreAdapterList::GetFactory
---

## -description

Retrieves an [IDXCoreAdapterFactory](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory) interface pointer to the DXCore adapter factory object. For programming guidance, and code examples, see [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters).

## -parameters

### -param riid

Type: **REFIID**

A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvFactory*. This is expected to be the interface identifier (IID) of [IDXCoreAdapterFactory](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory).

### -param ppvFactory [out]

Type: **void\*\***

The address of a pointer to an interface with the IID specified in the *riid* parameter. Upon successful return, *\*ppvFactory* (the dereferenced address) contains a pointer to the existing DXCore adapter factory object. Before returning, the function increments the reference count on the factory object's [IDXCoreAdapterFactory](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory) interface.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|E_NOINTERFACE|An invalid value was provided for *riid*.|
|E_POINTER|`nullptr` was provided for *ppvFactory*.|

## -remarks

For the duration of time that a reference exists on an [IDXCoreAdapterFactory](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory) interface, an [IDXCoreAdapterList](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist) interface, or an [IDXCoreAdapter](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapter) interface, additional calls to [DXCoreCreateAdapterFactory](/windows/win32/api/dxcore/nf-dxcore-dxcorecreateadapterfactory), [IDXCoreAdapterList::GetFactory](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory), or [IDXCoreAdapter::GetFactory](/windows/win32/api/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory) will return pointers to the same object, increasing the reference count of the **IDXCoreAdapterFactory** interface.

## -see-also

[IDXCoreAdapterList](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist), [DXCore Reference](/windows/win32/dxcore/dxcore-reference), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
