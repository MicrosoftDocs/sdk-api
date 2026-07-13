---
UID: NF:d3d12.D3D12SerializeRootSignature
title: D3D12SerializeRootSignature function (d3d12.h)
description: Serializes a root signature version 1.0 that can be passed to ID3D12Device::CreateRootSignature.
helpviewer_keywords: ["D3D12SerializeRootSignature","D3D12SerializeRootSignature function","d3d12/D3D12SerializeRootSignature","direct3d12.d3d12serializerootsignature"]
old-location: direct3d12\d3d12serializerootsignature.htm
tech.root: direct3d12
ms.assetid: ACC46F5E-1074-41B3-8D13-9FD4352DBF66
ms.date: 12/05/2018
ms.keywords: D3D12SerializeRootSignature, D3D12SerializeRootSignature function, d3d12/D3D12SerializeRootSignature, direct3d12.d3d12serializerootsignature
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12SerializeRootSignature
 - d3d12/D3D12SerializeRootSignature
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D12.dll
api_name:
 - D3D12SerializeRootSignature
---

# D3D12SerializeRootSignature function


## -description

Serializes a root signature version 1.0 that can be passed to <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature">ID3D12Device::CreateRootSignature</a>.

## -parameters

### -param pRootSignature [in]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc">D3D12_ROOT_SIGNATURE_DESC</a>*</b>

The description of the root signature, as a pointer to a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc">D3D12_ROOT_SIGNATURE_DESC</a> structure.

### -param Version [in]

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version">D3D_ROOT_SIGNATURE_VERSION</a></b>

A <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version">D3D_ROOT_SIGNATURE_VERSION</a>-typed value that specifies the version of root signature.

### -param ppBlob [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that you can use to access the serialized root signature.

### -param ppErrorBlob [out, optional]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

A pointer to a memory block that receives a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that you can use to access serializer error messages, or <b>NULL</b> if there are no errors.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

This function has been superceded by <a href="/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature">D3D12SerializeVersionedRootSignature</a> as of the Windows 10 Anniversary Update (14393).

If an application procedurally generates a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc">D3D12_ROOT_SIGNATURE_DESC</a> data structure, it must pass a pointer to this <b>D3D12_ROOT_SIGNATURE_DESC</b> in a call to <b>D3D12SerializeRootSignature</b> to make the serialized form.
        The application then passes the serialized form to which <i>ppBlob</i> points into <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature">ID3D12Device::CreateRootSignature</a>.
      

If a shader has been authored with a root signature in it, the compiled shader will contain a serialized root signature in it already. In this case, pass the compiled shader blob to <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature">ID3D12Device::CreateRootSignature</a> to obtain the runtime root signature object.
      

The function signature PFN_D3D12_SERIALIZE_ROOT_SIGNATURE is provided as a typedef, so that you can use dynamic linking techniques (<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>) instead of statically linking.
      


#### Examples

Create an empty root signature.


```cpp
CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
rootSignatureDesc.Init(0, nullptr, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

ComPtr<ID3DBlob> signature;
ComPtr<ID3DBlob> error;
ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));

```


Refer to the <a href="/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-functions">Core Functions</a>



<a href="/windows/desktop/direct3d12/creating-a-root-signature">Creating a Root Signature</a>
