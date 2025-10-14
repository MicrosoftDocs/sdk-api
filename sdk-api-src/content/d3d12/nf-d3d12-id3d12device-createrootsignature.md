---
UID: NF:d3d12.ID3D12Device.CreateRootSignature
title: ID3D12Device::CreateRootSignature (d3d12.h)
description: Creates a root signature layout.
helpviewer_keywords: ["CreateRootSignature","CreateRootSignature method","CreateRootSignature method","ID3D12Device interface","ID3D12Device interface","CreateRootSignature method","ID3D12Device.CreateRootSignature","ID3D12Device::CreateRootSignature","d3d12/ID3D12Device::CreateRootSignature","direct3d12.id3d12device_createrootsignature"]
old-location: direct3d12\id3d12device_createrootsignature.htm
tech.root: direct3d12
ms.assetid: CD3389EC-4086-40F0-B1DB-BCBCF9DDE6BA
ms.date: 12/05/2018
ms.keywords: CreateRootSignature, CreateRootSignature method, CreateRootSignature method,ID3D12Device interface, ID3D12Device interface,CreateRootSignature method, ID3D12Device.CreateRootSignature, ID3D12Device::CreateRootSignature, d3d12/ID3D12Device::CreateRootSignature, direct3d12.id3d12device_createrootsignature
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
 - ID3D12Device::CreateRootSignature
 - d3d12/ID3D12Device::CreateRootSignature
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12Device.CreateRootSignature
---

# ID3D12Device::CreateRootSignature


## -description

Creates a root signature layout.

## -parameters

### -param nodeMask [in]

Type: <b><a href="/windows/win32/WinProg/windows-data-types">UINT</a></b>

For single GPU operation, set this to zero. If there are multiple GPU nodes, set bits to identify the nodes (the  device's physical adapters) to which the root signature is to apply.
            Each bit in the mask corresponds to a single node.
            Refer to <a href="/windows/win32/direct3d12/multi-engine">Multi-adapter systems</a>.

### -param pBlobWithRootSignature [in]

Type: <b>const <a href="/windows/win32/WinProg/windows-data-types">void</a>*</b>

A pointer to the source data for the serialized signature.

### -param blobLengthInBytes [in]

Type: <b><a href="/windows/win32/WinProg/windows-data-types">SIZE_T</a></b>

The size, in bytes, of the block of memory that <i>pBlobWithRootSignature</i> points to.

### -param riid

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the root signature interface. See Remarks.
            An input parameter.

### -param ppvRootSignature [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the root signature.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the <a href="/windows/win32/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.
          

This method returns <b>E_INVALIDARG</b> if the blob that <i>pBlobWithRootSignature</i> points to is invalid.

## -remarks

If an application procedurally generates a <a href="/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc">D3D12_ROOT_SIGNATURE_DESC</a> data structure, it must pass a pointer to this <b>D3D12_ROOT_SIGNATURE_DESC</b> in a call to <a href="/windows/win32/api/d3d12/nf-d3d12-d3d12serializerootsignature">D3D12SerializeRootSignature</a> to make the serialized form.
        The application then passes the serialized form to <i>pBlobWithRootSignature</i> in a call to <b>ID3D12Device::CreateRootSignature</b>.
      

The <b>REFIID</b>, or <b>GUID</b>, of the interface to the root signature layout can be obtained by using the __uuidof() macro.
        For example, __uuidof(<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature">ID3D12RootSignature</a>) will get the <b>GUID</b> of the interface to a root signature.
      


#### Examples

The <a href="/windows/win32/direct3d12/working-samples">D3D12HelloTriangle</a> sample uses <b>ID3D12Device::CreateRootSignature</b> as follows:
        

Create an empty root signature.


```cpp
CD3DX12_ROOT_SIGNATURE_DESC rootSignatureDesc;
rootSignatureDesc.Init(0, nullptr, 0, nullptr, D3D12_ROOT_SIGNATURE_FLAG_ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT);

ComPtr<ID3DBlob> signature;
ComPtr<ID3DBlob> error;
ThrowIfFailed(D3D12SerializeRootSignature(&rootSignatureDesc, D3D_ROOT_SIGNATURE_VERSION_1, &signature, &error));
ThrowIfFailed(m_device->CreateRootSignature(0, signature->GetBufferPointer(), signature->GetBufferSize(), IID_PPV_ARGS(&m_rootSignature)));

```

## -see-also

<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>

