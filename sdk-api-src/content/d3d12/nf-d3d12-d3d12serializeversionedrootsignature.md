---
UID: NF:d3d12.D3D12SerializeVersionedRootSignature
title: D3D12SerializeVersionedRootSignature function (d3d12.h)
description: Serializes a root signature of any version that can be passed to ID3D12Device::CreateRootSignature.
helpviewer_keywords: ["D3D12SerializeVersionedRootSignature","D3D12SerializeVersionedRootSignature function","d3d12/D3D12SerializeVersionedRootSignature","direct3d12.d3d12serializeversionedrootsignature"]
old-location: direct3d12\d3d12serializeversionedrootsignature.htm
tech.root: direct3d12
ms.assetid: D8A15561-4911-4067-B25E-8BF2B079FD81
ms.date: 12/05/2018
ms.keywords: D3D12SerializeVersionedRootSignature, D3D12SerializeVersionedRootSignature function, d3d12/D3D12SerializeVersionedRootSignature, direct3d12.d3d12serializeversionedrootsignature
req.header: d3d12.h
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12SerializeVersionedRootSignature
 - d3d12/D3D12SerializeVersionedRootSignature
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d3d12.dll
api_name:
 - D3D12SerializeVersionedRootSignature
---

# D3D12SerializeVersionedRootSignature function


## -description

Serializes a root signature of any version that can be passed to <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature">ID3D12Device::CreateRootSignature</a>.

## -parameters

### -param pRootSignature [in]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc">D3D12_VERSIONED_ROOT_SIGNATURE_DESC</a>*</b>

Specifies a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc">D3D12_VERSIONED_ROOT_SIGNATURE_DESC</a> that contains a description of any version of a root signature.

### -param ppBlob [out]

Type: <b>ID3DBlob**</b>

A pointer to a memory block that receives a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that you can use to access the serialized root signature.

### -param ppErrorBlob [out, optional]

Type: <b>ID3DBlob**</b>

A pointer to a memory block that receives a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that you can use to access serializer error messages, or <b>NULL</b> if there are no errors.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

If an application procedurally generates a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1">D3D12_ROOT_SIGNATURE_DESC1</a> data structure, it must pass a pointer to this <b>D3D12_ROOT_SIGNATURE_DESC1</b> in a call to <b>D3D12SerializeVersionedRootSignature</b> to make the serialized form.
        The application then passes the serialized form to which <i>ppBlob</i> points into <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature">ID3D12Device::CreateRootSignature</a>.


If a shader has been authored with a root signature in it, the compiled shader will contain a serialized root signature in it already. In this case, pass the compiled shader blob to <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature">ID3D12Device::CreateRootSignature</a> to obtain the runtime root signature object.

> Note that for Xbox developers, use of HLSL-authored root signatures is strongly recommended.


The function signature PFN_D3D12_SERIALIZE_VERSIONED_ROOT_SIGNATURE is provided as a typedef, so that you can use dynamic linking techniques (<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>) instead of statically linking.
      

This function was released with the Windows 10 Anniversary Update (14393) and supersedes <a href="/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature">D3D12SerializeRootSignature</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-functions">Core Functions</a>



<a href="/windows/desktop/direct3d12/creating-a-root-signature">Creating a Root Signature</a>



<a href="/windows/desktop/direct3d12/d3dx12serializeversionedrootsignature">D3DX12SerializeVersionedRootSignature</a>



<a href="/windows/desktop/direct3d12/root-signature-version-1-1">Root Signature Version 1.1</a>
