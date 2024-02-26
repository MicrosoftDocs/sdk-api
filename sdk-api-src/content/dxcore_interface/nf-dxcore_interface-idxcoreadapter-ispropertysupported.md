---
UID: NF:dxcore_interface.IDXCoreAdapter.IsPropertySupported
title: IDXCoreAdapter::IsPropertySupported
description: Determines whether this DXCore adapter object and the current operating system (OS) support the specified adapter property.
tech.root: dxcore
ms.date: 06/17/2019
ms.keywords: IDXCoreAdapter interface,IsPropertySupported method, IDXCoreAdapter.IsPropertySupported, IDXCoreAdapter::IsPropertySupported, IsPropertySupported, IsPropertySupported method, IsPropertySupported method,IDXCoreAdapter interface, dxcore/IDXCoreAdapter::IsPropertySupported, dxcore_interface.idxcoreadapterfactory_ispropertysupported
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
 - IDXCoreAdapter::IsPropertySupported
---

## -description

Determines whether this DXCore adapter object and the current operating system (OS) support the specified adapter property.

## -parameters

### -param property

Type: **[DXCoreAdapterProperty](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty)**

The type of property that you're querying about support for. See the table in [DXCoreAdapterProperty](/windows/win32/api/dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty) for more info about each adapter property.

## -returns

Type: **bool**

Returns `true` if this DXCore adapter object and the current operating system (OS) support the specified adapter property. Otherwise, returns `false`.

## -see-also

[IDXCoreAdapter](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapter), [DXCore Reference](/windows/win32/dxcore/dxcore-reference), [DXCore adapter attribute GUIDs](/windows/win32/dxcore/dxcore-adapter-attribute-guids), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
