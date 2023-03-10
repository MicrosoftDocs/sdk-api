---
UID: NF:d3d12sdklayers.ID3D12DebugDevice.GetFeatureMask
title: ID3D12DebugDevice::GetFeatureMask (d3d12sdklayers.h)
description: Gets a bit field of flags that indicates which debug features are on or off.
helpviewer_keywords: ["GetFeatureMask","GetFeatureMask method","GetFeatureMask method","ID3D12DebugDevice interface","ID3D12DebugDevice interface","GetFeatureMask method","ID3D12DebugDevice.GetFeatureMask","ID3D12DebugDevice::GetFeatureMask","d3d12sdklayers/ID3D12DebugDevice::GetFeatureMask","direct3d12.id3d12debugdevice_getfeaturemask"]
old-location: direct3d12\id3d12debugdevice_getfeaturemask.htm
tech.root: direct3d12
ms.assetid: E4ECE63F-6738-4856-9912-93C3AAEE7E3B
ms.date: 12/05/2018
ms.keywords: GetFeatureMask, GetFeatureMask method, GetFeatureMask method,ID3D12DebugDevice interface, ID3D12DebugDevice interface,GetFeatureMask method, ID3D12DebugDevice.GetFeatureMask, ID3D12DebugDevice::GetFeatureMask, d3d12sdklayers/ID3D12DebugDevice::GetFeatureMask, direct3d12.id3d12debugdevice_getfeaturemask
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
 - ID3D12DebugDevice::GetFeatureMask
 - d3d12sdklayers/ID3D12DebugDevice::GetFeatureMask
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
 - ID3D12DebugDevice.GetFeatureMask
---

# ID3D12DebugDevice::GetFeatureMask


## -description

Gets a bit field of flags that indicates which debug features are on or off.



## -returns

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_feature">D3D12_DEBUG_FEATURE</a></b>

Mask of feature-mask flags,
            as a bitwise OR'ed combination of <a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_feature">D3D12_DEBUG_FEATURE</a> enumeration constants.
            If a flag is present, then that feature will be set to on, otherwise the feature will be set to off.

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice">ID3D12DebugDevice</a>



<a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice-setfeaturemask">ID3D12DebugDevice::SetFeatureMask</a>
