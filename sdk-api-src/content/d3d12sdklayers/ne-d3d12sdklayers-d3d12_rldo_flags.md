---
UID: NE:d3d12sdklayers.D3D12_RLDO_FLAGS
title: D3D12_RLDO_FLAGS (d3d12sdklayers.h)
description: Specifies options for the amount of information to report about a live device object's lifetime.
helpviewer_keywords: ["D3D12_RLDO_DETAIL","D3D12_RLDO_FLAGS","D3D12_RLDO_FLAGS enumeration","D3D12_RLDO_IGNORE_INTERNAL","D3D12_RLDO_NONE","D3D12_RLDO_SUMMARY","d3d12sdklayers/D3D12_RLDO_DETAIL","d3d12sdklayers/D3D12_RLDO_FLAGS","d3d12sdklayers/D3D12_RLDO_IGNORE_INTERNAL","d3d12sdklayers/D3D12_RLDO_NONE","d3d12sdklayers/D3D12_RLDO_SUMMARY","direct3d12.d3d12_rldo_flags"]
old-location: direct3d12\d3d12_rldo_flags.htm
tech.root: direct3d12
ms.assetid: FF868102-26FC-4541-9C21-0B8D6D4CF47B
ms.date: 12/05/2018
ms.keywords: D3D12_RLDO_DETAIL, D3D12_RLDO_FLAGS, D3D12_RLDO_FLAGS enumeration, D3D12_RLDO_IGNORE_INTERNAL, D3D12_RLDO_NONE, D3D12_RLDO_SUMMARY, d3d12sdklayers/D3D12_RLDO_DETAIL, d3d12sdklayers/D3D12_RLDO_FLAGS, d3d12sdklayers/D3D12_RLDO_IGNORE_INTERNAL, d3d12sdklayers/D3D12_RLDO_NONE, d3d12sdklayers/D3D12_RLDO_SUMMARY, direct3d12.d3d12_rldo_flags
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
req.typenames: D3D12_RLDO_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RLDO_FLAGS
 - d3d12sdklayers/D3D12_RLDO_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12sdklayers.h
api_name:
 - D3D12_RLDO_FLAGS
---

# D3D12_RLDO_FLAGS enumeration


## -description

Specifies options for the amount of information to report about a live device object's lifetime.

## -enum-fields

### -field D3D12_RLDO_NONE:0

### -field D3D12_RLDO_SUMMARY:0x1

Obtain a summary about a live device object's lifetime.

### -field D3D12_RLDO_DETAIL:0x2

Obtain detailed information about a live device object's lifetime.

### -field D3D12_RLDO_IGNORE_INTERNAL:0x4

This flag indicates to ignore objects which have no external refcounts keeping them alive. D3D objects are printed using an external refcount and an internal refcount. Typically, all objects are printed. This flag means ignore the objects whose external refcount is 0, because the application is not responsible for keeping them alive.

## -remarks

This enumeration is used by <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice-reportlivedeviceobjects">ID3D12DebugDevice::ReportLiveDeviceObjects</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-sdklayers-enumerations">Debug Layer Enumerations</a>
