---
UID: NF:d3d12sdklayers.ID3D12Debug3.SetEnableGPUBasedValidation
title: ID3D12Debug3::SetEnableGPUBasedValidation (d3d12sdklayers.h)
description: This method enables or disables GPU-based validation (GBV) before creating a device with the debug layer enabled.
helpviewer_keywords: ["- ID3D12Debug3.SetEnableGPUBasedValidation"]
tech.root: direct3d12
ms.date: 03/02/2020
req.header: d3d12sdklayers.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - ID3D12Debug3::SetEnableGPUBasedValidation
 - d3d12sdklayers/ID3D12Debug3::SetEnableGPUBasedValidation
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
 - ID3D12Debug3.SetEnableGPUBasedValidation
---

## -description

This method enables or disables GPU-based validation (GBV) before creating a device with the debug layer enabled.

## -parameters

### -param Enable

Type: <b>BOOL</b>

TRUE to enable GPU-based validation, otherwise FALSE.

## -remarks

GPU-based validation can be enabled/disabled only prior to creating a device. By default, GPU-based validation is disabled. To disable GPU-based validation after initially enabling it, the device must be fully released and recreated.

For more information, see <a href="/windows/win32/direct3d12/using-d3d12-debug-layer-gpu-based-validation">Using D3D12 Debug Layer GPU-based validation</a>.

## -see-also

<a href="/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug3">ID3D12Debug3</a>

