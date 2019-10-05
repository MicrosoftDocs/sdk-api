---
UID: NF:d3d12.ID3D12DeviceRemovedExtendedDataSettings.SetPageFaultEnablement
title: ID3D12DeviceRemovedExtendedDataSettings::SetPageFaultEnablement
author: windows-sdk-content
description: Configures the enablement settings for Device Removed Extended Data (DRED) page fault reporting.
old-location: direct3d12\id3d12deviceremovedextendeddatasettings_setpagefaultenablement.htm
tech.root: direct3d12
ms.author: windowssdkdev
ms.date: 02/08/2019
ms.keywords: SetPageFaultEnablement, SetPageFaultEnablement method, ID3D12DeviceRemovedExtendedDataSettings, ID3D12DeviceRemovedExtendedDataSettings interface, ID3D12DeviceRemovedExtendedDataSettings.SetPageFaultEnablement, ID3D12DeviceRemovedExtendedDataSettings::SetPageFaultEnablement, d3d12/ID3D12DeviceRemovedExtendedDataSettings::SetPageFaultEnablement, direct3d12.id3d12deviceremovedextendeddatasettings_setpagefaultenablement
ms.topic: method
f1_keywords: 
 - "d3d12/ID3D12DeviceRemovedExtendedDataSettings::SetPageFaultEnablement"
dev_langs:
 - c++
req.construct-type: function
req.ddi-compliance: 
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1903
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
 - apiref
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.h
api_name:
 - ID3D12DeviceRemovedExtendedDataSettings::SetPageFaultEnablement
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12DeviceRemovedExtendedDataSettings::SetPageFaultEnablement

## -description

Configures the enablement settings for Device Removed Extended Data (DRED) page fault reporting.

## -parameters

### -param __MIDL__ID3D12DeviceRemovedExtendedDataSettings0001

A [D3D12_DRED_ENABLEMENT](ne-d3d12-d3d12_dred_enablement.md) value. The default is **D3D12_DRED_ENABLEMENT_SYSTEM_CONTROLLED**.

## -returns

This method does not return a value.

## -see-also

* [ID3D12DeviceRemovedExtendedDataSettings interface](nn-d3d12-id3d12deviceremovedextendeddatasettings.md)
* [Use DRED to diagnose GPU faults](/windows/desktop/direct3d12/use-dred)
