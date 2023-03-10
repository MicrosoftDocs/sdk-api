---
UID: NF:d3d11.ID3D11DeviceContext.GSSetShader
title: ID3D11DeviceContext::GSSetShader (d3d11.h)
description: Set a geometry shader to the device. (ID3D11DeviceContext.GSSetShader)
helpviewer_keywords: ["52389497-00e9-1a7b-1543-a60e2a6b6479","GSSetShader","GSSetShader method [Direct3D 11]","GSSetShader method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","GSSetShader method","ID3D11DeviceContext.GSSetShader","ID3D11DeviceContext::GSSetShader","d3d11/ID3D11DeviceContext::GSSetShader","direct3d11.id3d11devicecontext_gssetshader"]
old-location: direct3d11\id3d11devicecontext_gssetshader.htm
tech.root: direct3d11
ms.assetid: 6c42d028-b832-470c-ab15-1cf46a3f8414
ms.date: 12/05/2018
ms.keywords: 52389497-00e9-1a7b-1543-a60e2a6b6479, GSSetShader, GSSetShader method [Direct3D 11], GSSetShader method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],GSSetShader method, ID3D11DeviceContext.GSSetShader, ID3D11DeviceContext::GSSetShader, d3d11/ID3D11DeviceContext::GSSetShader, direct3d11.id3d11devicecontext_gssetshader
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext::GSSetShader
 - d3d11/ID3D11DeviceContext::GSSetShader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.GSSetShader
---

# ID3D11DeviceContext::GSSetShader


## -description

Set a geometry shader to the device.

## -parameters

### -param pShader [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader">ID3D11GeometryShader</a>*</b>

Pointer to a geometry shader (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader">ID3D11GeometryShader</a>). Passing in <b>NULL</b> disables the shader for this pipeline stage.

### -param ppClassInstances [in, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a>*</b>

A pointer to an array of class-instance interfaces (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a>). Each interface used by a shader must have a corresponding class instance or the shader will get disabled. Set ppClassInstances to <b>NULL</b> if the shader does not use any interfaces.

### -param NumClassInstances

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of class-instance interfaces in the array.

## -remarks

The method will hold a reference to the interfaces passed in.
      This differs from the device state behavior in Direct3D 10.

The maximum number of instances a shader can have is 256.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
