---
UID: NE:d3d11sdklayers.D3D11_RLDO_FLAGS
title: D3D11_RLDO_FLAGS (d3d11sdklayers.h)
description: Options for the amount of information to report about a device object's lifetime.
helpviewer_keywords: ["5a79a782-10e1-3c49-ad30-96926d31c37d","D3D11_RLDO_DETAIL","D3D11_RLDO_FLAGS","D3D11_RLDO_FLAGS enumeration [Direct3D 11]","D3D11_RLDO_IGNORE_INTERNAL","D3D11_RLDO_SUMMARY","d3d11sdklayers/D3D11_RLDO_DETAIL","d3d11sdklayers/D3D11_RLDO_FLAGS","d3d11sdklayers/D3D11_RLDO_IGNORE_INTERNAL","d3d11sdklayers/D3D11_RLDO_SUMMARY","direct3d11.d3d11_rldo_flags"]
old-location: direct3d11\d3d11_rldo_flags.htm
tech.root: direct3d11
ms.assetid: 9ab8c5c7-bb4e-4d6b-90fc-5e4cdfba0c71
ms.date: 12/05/2018
ms.keywords: 5a79a782-10e1-3c49-ad30-96926d31c37d, D3D11_RLDO_DETAIL, D3D11_RLDO_FLAGS, D3D11_RLDO_FLAGS enumeration [Direct3D 11], D3D11_RLDO_IGNORE_INTERNAL, D3D11_RLDO_SUMMARY, d3d11sdklayers/D3D11_RLDO_DETAIL, d3d11sdklayers/D3D11_RLDO_FLAGS, d3d11sdklayers/D3D11_RLDO_IGNORE_INTERNAL, d3d11sdklayers/D3D11_RLDO_SUMMARY, direct3d11.d3d11_rldo_flags
req.header: d3d11sdklayers.h
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
req.typenames: D3D11_RLDO_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_RLDO_FLAGS
 - d3d11sdklayers/D3D11_RLDO_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11SDKLayers.h
api_name:
 - D3D11_RLDO_FLAGS
---

# D3D11_RLDO_FLAGS enumeration


## -description

Options for the amount of information to report about a device object's lifetime.

## -enum-fields

### -field D3D11_RLDO_SUMMARY:0x1

Specifies to obtain a summary about a device object's lifetime.

### -field D3D11_RLDO_DETAIL:0x2

Specifies to obtain detailed information about a device object's lifetime.

### -field D3D11_RLDO_IGNORE_INTERNAL:0x4

This flag indicates to ignore objects which have no external refcounts keeping them alive. D3D objects are printed using an external refcount and an internal refcount. Typically, all objects are printed. This flag means ignore the objects whose external refcount is 0, because the application is not responsible for keeping them alive.

## -remarks

This enumeration is used by <a href="/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-reportlivedeviceobjects">ID3D11Debug::ReportLiveDeviceObjects</a>.
        

Several inline functions exist to combine the options using operators, see the D3D11SDKLayers.h header file for details.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-layer-enums">Core Enumerations</a>
