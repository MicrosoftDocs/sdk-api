---
UID: NS:d3d10.D3D10_COUNTER_INFO
title: D3D10_COUNTER_INFO (d3d10.h)
description: Information about the video card's performance counter capabilities. (D3D10_COUNTER_INFO)
helpviewer_keywords: ["556a7645-8a0b-b615-840b-b33669862365","D3D10_COUNTER_INFO","D3D10_COUNTER_INFO structure [Direct3D 10]","d3d10/D3D10_COUNTER_INFO","direct3d10.d3d10_counter_info"]
old-location: direct3d10\d3d10_counter_info.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_counter_info.htm
ms.date: 12/05/2018
ms.keywords: 556a7645-8a0b-b615-840b-b33669862365, D3D10_COUNTER_INFO, D3D10_COUNTER_INFO structure [Direct3D 10], d3d10/D3D10_COUNTER_INFO, direct3d10.d3d10_counter_info
req.header: d3d10.h
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
req.typenames: D3D10_COUNTER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_COUNTER_INFO
 - d3d10/D3D10_COUNTER_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_COUNTER_INFO
---

# D3D10_COUNTER_INFO structure


## -description

Information about the video card's performance counter capabilities.

## -struct-fields

### -field LastDeviceDependentCounter

Type: <b><a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_counter">D3D10_COUNTER</a></b>

Largest device-dependent counter ID that the device supports. If none are supported, this value will be 0. Otherwise it will be greater than or equal to D3D10_COUNTER_DEVICE_DEPENDENT_0. See <a href="/windows/desktop/api/d3d10/ne-d3d10-d3d10_counter">D3D10_COUNTER</a>.

### -field NumSimultaneousCounters

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of counters that can be simultaneously supported.

### -field NumDetectableParallelUnits

Type: <b>UINT8</b>

Number of detectable parallel units that the counter is able to discern. Values are 1 ~ 4. Use NumDetectableParallelUnits to interpret the values of the VERTEX_PROCESSING, GEOMETRY_PROCESSING, PIXEL_PROCESSING, and OTHER_GPU_PROCESSING counters. See <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10asynchronous-getdata">ID3D10Asynchronous::GetData</a> for an equation.

## -remarks

This structure is returned by <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-checkcounterinfo">ID3D10Device::CheckCounterInfo</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-structures">Core Structures</a>
