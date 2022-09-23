---
UID: NF:d3d12sdklayers.ID3D12DebugDevice.SetFeatureMask
title: ID3D12DebugDevice::SetFeatureMask (d3d12sdklayers.h)
description: Set a bit field of flags that will turn debug features on and off. (ID3D12DebugDevice.SetFeatureMask)
helpviewer_keywords: ["ID3D12DebugDevice interface","SetFeatureMask method","ID3D12DebugDevice.SetFeatureMask","ID3D12DebugDevice::SetFeatureMask","SetFeatureMask","SetFeatureMask method","SetFeatureMask method","ID3D12DebugDevice interface","d3d12sdklayers/ID3D12DebugDevice::SetFeatureMask","direct3d12.id3d12debugdevice_setfeaturemask"]
old-location: direct3d12\id3d12debugdevice_setfeaturemask.htm
tech.root: direct3d12
ms.assetid: 12232AB8-BBEA-4663-BEB2-7E296851FE5E
ms.date: 12/05/2018
ms.keywords: ID3D12DebugDevice interface,SetFeatureMask method, ID3D12DebugDevice.SetFeatureMask, ID3D12DebugDevice::SetFeatureMask, SetFeatureMask, SetFeatureMask method, SetFeatureMask method,ID3D12DebugDevice interface, d3d12sdklayers/ID3D12DebugDevice::SetFeatureMask, direct3d12.id3d12debugdevice_setfeaturemask
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
 - ID3D12DebugDevice::SetFeatureMask
 - d3d12sdklayers/ID3D12DebugDevice::SetFeatureMask
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
 - ID3D12DebugDevice.SetFeatureMask
---

# ID3D12DebugDevice::SetFeatureMask


## -description

Set a bit field of flags that will turn debug features on and off.

## -parameters

### -param Mask

Type: <b><a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_feature">D3D12_DEBUG_FEATURE</a></b>

Feature-mask flags, as a bitwise-OR'd combination of <a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_debug_feature">D3D12_DEBUG_FEATURE</a> enumeration constants.
            If a flag is present, that feature will be set to on; otherwise, the feature will be set to off.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.
            <a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a>

## -see-also

<a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice-getfeaturemask">GetFeatureMask</a>



<a href="/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice">ID3D12DebugDevice</a>
