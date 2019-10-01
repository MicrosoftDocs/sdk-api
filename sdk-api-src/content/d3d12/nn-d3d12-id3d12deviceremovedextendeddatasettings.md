---
UID: NN:d3d12.ID3D12DeviceRemovedExtendedDataSettings
title: ID3D12DeviceRemovedExtendedDataSettings interface
author: windows-sdk-content
description: This interface controls Device Removed Extended Data (DRED) settings.
tech.root: direct3d12
ms.author: windowssdkdev
ms.date: 02/08/2019
ms.keywords: ID3D12DeviceRemovedExtendedDataSettings, ID3D12DeviceRemovedExtendedDataSettings interface, ID3D12DeviceRemovedExtendedDataSettings interface,described, d3d12/ID3D12DeviceRemovedExtendedDataSettings, direct3d12.id3d12deviceremovedextendeddatasettings
ms.topic: interface
f1_keywords: 
 - "d3d12/ID3D12DeviceRemovedExtendedDataSettings"
req.header: d3d12.h
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12DeviceRemovedExtendedDataSettings
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12DeviceRemovedExtendedDataSettings interface

## -description

This interface controls Device Removed Extended Data (DRED) settings. You should configure all DRED settings before you create a Direct3D 12 device. To retrieve the **ID3D12DeviceRemovedExtendedDataSettings** interface, call [D3D12GetDebugInterface](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface), passing the interface identifier (IID) of **ID3D12DeviceRemovedExtendedDataSettings**.

## Inheritance

The **ID3D12DeviceRemovedExtendedDataSettings** interface inherits from the [IUnknown](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.

## -members

The **ID3D12DeviceRemovedExtendedDataSettings** interface has these methods.

|Method|Description|
|-|-|
|[SetAutoBreadcrumbsEnablement](nf-d3d12-id3d12deviceremovedextendeddatasettings-setautobreadcrumbsenablement.md)|Configures the enablement settings for Device Removed Extended Data (DRED) auto-breadcrumbs.|
|[SetPageFaultEnablement](nf-d3d12-id3d12deviceremovedextendeddatasettings-setpagefaultenablement.md)|Configures the enablement settings for Device Removed Extended Data (DRED) page fault reporting.|
|[SetWatsonDumpEnablement](nf-d3d12-id3d12deviceremovedextendeddatasettings-setwatsondumpenablement.md)|Configures the enablement settings for Device Removed Extended Data (DRED) Watson dumps.|

## -remarks

## -see-also

* [Core interfaces](/windows/desktop/direct3d12/direct3d-12-interfaces)
* [Use DRED to diagnose GPU faults](/windows/desktop/direct3d12/use-dred)
