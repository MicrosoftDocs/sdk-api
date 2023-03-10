---
UID: NF:d3d10.ID3D10Device.GSSetShader
title: ID3D10Device::GSSetShader (d3d10.h)
description: Set a geometry shader to the device. (ID3D10Device.GSSetShader)
helpviewer_keywords: ["GSSetShader","GSSetShader method [Direct3D 10]","GSSetShader method [Direct3D 10]","ID3D10Device interface","ID3D10Device interface [Direct3D 10]","GSSetShader method","ID3D10Device.GSSetShader","ID3D10Device::GSSetShader","bec21328-0eb9-6e55-a154-2849f276da74","d3d10/ID3D10Device::GSSetShader","direct3d10.id3d10device_gssetshader"]
old-location: direct3d10\id3d10device_gssetshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_gssetshader.htm
ms.date: 12/05/2018
ms.keywords: GSSetShader, GSSetShader method [Direct3D 10], GSSetShader method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],GSSetShader method, ID3D10Device.GSSetShader, ID3D10Device::GSSetShader, bec21328-0eb9-6e55-a154-2849f276da74, d3d10/ID3D10Device::GSSetShader, direct3d10.id3d10device_gssetshader
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::GSSetShader
 - d3d10/ID3D10Device::GSSetShader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.GSSetShader
---

# ID3D10Device::GSSetShader


## -description

Set a geometry shader to the device.

## -parameters

### -param pShader [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10geometryshader">ID3D10GeometryShader</a>*</b>

Pointer to a geometry shader (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10geometryshader">ID3D10GeometryShader</a>). Passing in <b>NULL</b> disables the shader for this pipeline stage.

## -remarks

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
