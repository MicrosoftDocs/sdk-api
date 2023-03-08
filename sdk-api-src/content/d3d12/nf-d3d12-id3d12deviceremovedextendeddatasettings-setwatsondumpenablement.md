---
UID: NF:d3d12.ID3D12DeviceRemovedExtendedDataSettings.SetWatsonDumpEnablement
title: ID3D12DeviceRemovedExtendedDataSettings::SetWatsonDumpEnablement
description: Configures the enablement settings for Device Removed Extended Data (DRED) Watson dump creation.
helpviewer_keywords: ["SetWatsonDumpEnablement","SetWatsonDumpEnablement method","ID3D12DeviceRemovedExtendedDataSettings","ID3D12DeviceRemovedExtendedDataSettings interface","ID3D12DeviceRemovedExtendedDataSettings.SetWatsonDumpEnablement","ID3D12DeviceRemovedExtendedDataSettings::SetWatsonDumpEnablement","d3d12/ID3D12DeviceRemovedExtendedDataSettings::SetWatsonDumpEnablement","direct3d12.id3d12deviceremovedextendeddatasettings_setwatsondumpenablement"]
old-location: direct3d12\id3d12deviceremovedextendeddatasettings_setwatsondumpenablement.htm
tech.root: direct3d12
ms.date: 02/08/2019
ms.keywords: SetWatsonDumpEnablement, SetWatsonDumpEnablement method, ID3D12DeviceRemovedExtendedDataSettings, ID3D12DeviceRemovedExtendedDataSettings interface, ID3D12DeviceRemovedExtendedDataSettings.SetWatsonDumpEnablement, ID3D12DeviceRemovedExtendedDataSettings::SetWatsonDumpEnablement, d3d12/ID3D12DeviceRemovedExtendedDataSettings::SetWatsonDumpEnablement, direct3d12.id3d12deviceremovedextendeddatasettings_setwatsondumpenablement
req.construct-type: function
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1903
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
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
 - ID3D12DeviceRemovedExtendedDataSettings::SetWatsonDumpEnablement
 - d3d12/ID3D12DeviceRemovedExtendedDataSettings::SetWatsonDumpEnablement
dev_langs:
 - c++
topic_type:
 - apiref
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.h
api_name:
 - ID3D12DeviceRemovedExtendedDataSettings::SetWatsonDumpEnablement
---

# ID3D12DeviceRemovedExtendedDataSettings::SetWatsonDumpEnablement


## -description

Configures the enablement settings for Device Removed Extended Data (DRED) dump creation for [Windows Error Reporting (WER)](/windows/desktop/wer/windows-error-reporting), also known as Watson.

## -parameters

### -param Enablement

A [D3D12_DRED_ENABLEMENT](ne-d3d12-d3d12_dred_enablement.md) value. The default is **D3D12_DRED_ENABLEMENT_SYSTEM_CONTROLLED**.

## -see-also

* [ID3D12DeviceRemovedExtendedDataSettings interface](nn-d3d12-id3d12deviceremovedextendeddatasettings.md)
* [Use DRED to diagnose GPU faults](/windows/desktop/direct3d12/use-dred)

