---
UID: NN:d3d12.ID3D12DeviceRemovedExtendedDataSettings
title: ID3D12DeviceRemovedExtendedDataSettings interface
description: This interface controls Device Removed Extended Data (DRED) settings.
helpviewer_keywords: ["ID3D12DeviceRemovedExtendedDataSettings","ID3D12DeviceRemovedExtendedDataSettings interface","ID3D12DeviceRemovedExtendedDataSettings interface","described","d3d12/ID3D12DeviceRemovedExtendedDataSettings","direct3d12.id3d12deviceremovedextendeddatasettings"]
tech.root: direct3d12
ms.date: 02/08/2019
ms.keywords: ID3D12DeviceRemovedExtendedDataSettings, ID3D12DeviceRemovedExtendedDataSettings interface, ID3D12DeviceRemovedExtendedDataSettings interface,described, d3d12/ID3D12DeviceRemovedExtendedDataSettings, direct3d12.id3d12deviceremovedextendeddatasettings
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12DeviceRemovedExtendedDataSettings
 - d3d12/ID3D12DeviceRemovedExtendedDataSettings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12DeviceRemovedExtendedDataSettings
---

# ID3D12DeviceRemovedExtendedDataSettings interface


## -description

This interface controls Device Removed Extended Data (DRED) settings. You should configure all DRED settings before you create a Direct3D 12 device. To retrieve the **ID3D12DeviceRemovedExtendedDataSettings** interface, call [D3D12GetDebugInterface](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface), passing the interface identifier (IID) of **ID3D12DeviceRemovedExtendedDataSettings**.

## Inheritance

The **ID3D12DeviceRemovedExtendedDataSettings** interface inherits from the [IUnknown](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.

## -remarks

## -see-also

* [Core interfaces](/windows/desktop/direct3d12/direct3d-12-interfaces)
* [Use DRED to diagnose GPU faults](/windows/desktop/direct3d12/use-dred)

