---
UID: NF:dxcore_interface.IDXCoreAdapter.IsAttributeSupported
title: IDXCoreAdapter::IsAttributeSupported
description: Determines whether this DXCore adapter object supports the specified adapter attribute.
author: windows-sdk-content
tech.root: dxcore
ms.author: windowssdkdev
ms.date: 06/10/2019
ms.keywords: IDXCoreAdapter interface,IsAttributeSupported method, IDXCoreAdapter.IsAttributeSupported, IDXCoreAdapter::IsAttributeSupported, IsAttributeSupported, IsAttributeSupported method, IsAttributeSupported method,IDXCoreAdapter interface, dxcore/IDXCoreAdapter::IsAttributeSupported, dxcore_interface.idxcoreadapterfactory_isattributesupported
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
 - IDXCoreAdapter::IsAttributeSupported
---

## -description

Determines whether this DXCore adapter object supports the specified adapter attribute.

## -parameters

### -param attributeGUID

Type: **REFGUID**

A reference to an adapter attribute GUID. For a list of attribute GUIDs, see [DXCore adapter attribute GUIDs](/windows/win32/dxcore/dxcore-adapter-attribute-guids).

## -returns

Type: **bool**

Returns `true` if this DXCore adapter object supports the specified adapter attribute. Otherwise, returns `false`.

## -see-also

[IDXCoreAdapter](/windows/win32/api/dxcore_interface/nn-dxcore_interface-idxcoreadapter), [DXCore Reference](/windows/win32/dxcore/dxcore-reference), [DXCore adapter attribute GUIDs](/windows/win32/dxcore/dxcore-adapter-attribute-guids), [Using DXCore to enumerate adapters](/windows/win32/dxcore/dxcore-enum-adapters)
