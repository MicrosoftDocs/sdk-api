---
UID: NF:d3d12sdklayers.ID3D12Debug1.SetEnableGPUBasedValidation
title: ID3D12Debug1::SetEnableGPUBasedValidation (d3d12sdklayers.h)
description: This method enables or disables GPU-Based Validation (GBV) before creating a device with the debug layer enabled.
helpviewer_keywords: ["ID3D12Debug1 interface","SetEnableGPUBasedValidation method","ID3D12Debug1.SetEnableGPUBasedValidation","ID3D12Debug1::SetEnableGPUBasedValidation","SetEnableGPUBasedValidation","SetEnableGPUBasedValidation method","SetEnableGPUBasedValidation method","ID3D12Debug1 interface","d3d12sdklayers/ID3D12Debug1::SetEnableGPUBasedValidation","direct3d12.id3d12debugdevice1_setenablegpubasedvalidation"]
old-location: direct3d12\id3d12debugdevice1_setenablegpubasedvalidation.htm
tech.root: direct3d12
ms.assetid: 0B7ACDC1-D7F6-4565-8E33-F2F14A96E4A8
ms.date: 12/05/2018
ms.keywords: ID3D12Debug1 interface,SetEnableGPUBasedValidation method, ID3D12Debug1.SetEnableGPUBasedValidation, ID3D12Debug1::SetEnableGPUBasedValidation, SetEnableGPUBasedValidation, SetEnableGPUBasedValidation method, SetEnableGPUBasedValidation method,ID3D12Debug1 interface, d3d12sdklayers/ID3D12Debug1::SetEnableGPUBasedValidation, direct3d12.id3d12debugdevice1_setenablegpubasedvalidation
req.header: d3d12sdklayers.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Debug1::SetEnableGPUBasedValidation
 - d3d12sdklayers/ID3D12Debug1::SetEnableGPUBasedValidation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12Debug1.SetEnableGPUBasedValidation
---

# ID3D12Debug1::SetEnableGPUBasedValidation


## -description

This method enables or disables GPU-Based Validation (GBV) before creating a device with the debug layer enabled.

## -parameters

### -param Enable

Type: <b>BOOL</b>

TRUE to enable GPU-Based Validation, otherwise FALSE.

## -remarks

GPU-Based Validation can only be enabled/disabled prior to creating a device.  By default, GPU-Based Validation is disabled.  To disable GPU-Based Validation after initially enabling it the device must be fully released and recreated; disabling or enabling it after device creation will cause device removal.

For more information, see <a href="/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation">Using D3D12 Debug Layer GPU-Based Validation</a>.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1">ID3D12Debug1</a>
