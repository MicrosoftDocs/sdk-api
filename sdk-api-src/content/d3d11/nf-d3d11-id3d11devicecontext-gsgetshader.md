---
UID: NF:d3d11.ID3D11DeviceContext.GSGetShader
title: ID3D11DeviceContext::GSGetShader (d3d11.h)
description: Get the geometry shader currently set on the device. (ID3D11DeviceContext.GSGetShader)
helpviewer_keywords: ["154380d2-d835-0821-b4a5-1f810f07c0e3","GSGetShader","GSGetShader method [Direct3D 11]","GSGetShader method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","GSGetShader method","ID3D11DeviceContext.GSGetShader","ID3D11DeviceContext::GSGetShader","d3d11/ID3D11DeviceContext::GSGetShader","direct3d11.id3d11devicecontext_gsgetshader"]
old-location: direct3d11\id3d11devicecontext_gsgetshader.htm
tech.root: direct3d11
ms.assetid: 5d5b935f-7eef-48ee-a2ed-82dd6c59aa19
ms.date: 12/05/2018
ms.keywords: 154380d2-d835-0821-b4a5-1f810f07c0e3, GSGetShader, GSGetShader method [Direct3D 11], GSGetShader method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],GSGetShader method, ID3D11DeviceContext.GSGetShader, ID3D11DeviceContext::GSGetShader, d3d11/ID3D11DeviceContext::GSGetShader, direct3d11.id3d11devicecontext_gsgetshader
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
 - ID3D11DeviceContext::GSGetShader
 - d3d11/ID3D11DeviceContext::GSGetShader
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
 - ID3D11DeviceContext.GSGetShader
---

# ID3D11DeviceContext::GSGetShader


## -description

Get the geometry shader currently set on the device.

## -parameters

### -param ppGeometryShader [out]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader">ID3D11GeometryShader</a>**</b>

Address of a pointer to a geometry shader (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader">ID3D11GeometryShader</a>) to be returned by the method.

### -param ppClassInstances [out, optional]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a>**</b>

Pointer to an array of class instance interfaces (see <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a>).

### -param pNumClassInstances [in, out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

The number of class-instance elements in the array.

## -remarks

Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
