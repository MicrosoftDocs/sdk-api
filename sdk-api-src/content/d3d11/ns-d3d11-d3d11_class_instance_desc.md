---
UID: NS:d3d11.D3D11_CLASS_INSTANCE_DESC
title: D3D11_CLASS_INSTANCE_DESC (d3d11.h)
description: Describes an HLSL class instance.
helpviewer_keywords: ["27ba9c43-314f-b252-fc98-8a27455ec5dd","D3D11_CLASS_INSTANCE_DESC","D3D11_CLASS_INSTANCE_DESC structure [Direct3D 11]","d3d11/D3D11_CLASS_INSTANCE_DESC","direct3d11.d3d11_class_instance_desc"]
old-location: direct3d11\d3d11_class_instance_desc.htm
tech.root: direct3d11
ms.assetid: 8ed0e6dd-227b-4e15-b949-34086523f064
ms.date: 12/05/2018
ms.keywords: 27ba9c43-314f-b252-fc98-8a27455ec5dd, D3D11_CLASS_INSTANCE_DESC, D3D11_CLASS_INSTANCE_DESC structure [Direct3D 11], d3d11/D3D11_CLASS_INSTANCE_DESC, direct3d11.d3d11_class_instance_desc
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D11_CLASS_INSTANCE_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_CLASS_INSTANCE_DESC
 - d3d11/D3D11_CLASS_INSTANCE_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_CLASS_INSTANCE_DESC
---

# D3D11_CLASS_INSTANCE_DESC structure


## -description

Describes an HLSL class instance.

## -struct-fields

### -field InstanceId

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The instance ID of an HLSL class; the default value is 0.

### -field InstanceIndex

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The instance index of an HLSL class; the default value is 0.

### -field TypeId

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The type ID of an HLSL class; the default value is 0.

### -field ConstantBuffer

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Describes the constant buffer associated with an HLSL class; the default value is 0.

### -field BaseConstantBufferOffset

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The base constant buffer offset associated with an HLSL class; the default value is 0.

### -field BaseTexture

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The base texture associated with an HLSL class; the default value is 127.

### -field BaseSampler

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The base sampler associated with an HLSL class; the default value is 15.

### -field Created

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

True if the class was created; the default value is false.

## -remarks

The D3D11_CLASS_INSTANCE_DESC structure is returned by the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11classinstance-getdesc">ID3D11ClassInstance::GetDesc</a> method.

The members of this structure except <b>InstanceIndex</b> are valid (non default values) if they describe a class instance acquired using  <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance">ID3D11ClassLinkage::CreateClassInstance</a>.  The <b>InstanceIndex</b> member is only valid when the class instance is aquired using <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance">ID3D11ClassLinkage::GetClassInstance</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-structures">Shader Structures</a>