---
UID: NF:d3d12.D3D12CreateRootSignatureDeserializer
title: D3D12CreateRootSignatureDeserializer function (d3d12.h)
description: Deserializes a root signature so you can determine the layout definition (D3D12_ROOT_SIGNATURE_DESC).
helpviewer_keywords: ["D3D12CreateRootSignatureDeserializer","D3D12CreateRootSignatureDeserializer function","d3d12/D3D12CreateRootSignatureDeserializer","direct3d12.d3d12createrootsignaturedeserializer"]
old-location: direct3d12\d3d12createrootsignaturedeserializer.htm
tech.root: direct3d12
ms.assetid: 96E58C9B-569F-41B8-A799-E87D849C045C
ms.date: 12/05/2018
ms.keywords: D3D12CreateRootSignatureDeserializer, D3D12CreateRootSignatureDeserializer function, d3d12/D3D12CreateRootSignatureDeserializer, direct3d12.d3d12createrootsignaturedeserializer
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
 - D3D12CreateRootSignatureDeserializer
 - d3d12/D3D12CreateRootSignatureDeserializer
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
 - D3D12CreateRootSignatureDeserializer
---

# D3D12CreateRootSignatureDeserializer function


## -description

Deserializes a root signature so you can determine the layout definition (<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc">D3D12_ROOT_SIGNATURE_DESC</a>).

## -parameters

### -param pSrcData [in]

Type: <b>LPCVOID</b>

A pointer to the source data for the serialized root signature.

### -param SrcDataSizeInBytes [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

The size, in bytes, of the block of memory that <i>pSrcData</i> points to.

### -param pRootSignatureDeserializerInterface [in]

Type: <b>REFIID</b>

The globally unique identifier (<b>GUID</b>) for the root signature deserializer interface. See remarks.

### -param ppRootSignatureDeserializer [out]

Type: <b>void**</b>

A pointer to a memory block that receives a pointer to the root signature deserializer.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns <b>S_OK</b> if successful; otherwise, returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.

## -remarks

This function has been superceded by <a href="/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer">D3D12CreateVersionedRootSignatureDeserializer</a>.

If an application has a serialized root signature already or has a compiled shader that contains a root signature and wants to determine the layout definition, it can call <b>D3D12CreateRootSignatureDeserializer</b> to generate a <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer">ID3D12RootSignatureDeserializer</a> interface. <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12rootsignaturedeserializer-getrootsignaturedesc">ID3D12RootSignatureDeserializer::GetRootSignature</a> can return the deserialized data structure
        (<a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc">D3D12_ROOT_SIGNATURE_DESC</a>).
        <b>ID3D12RootSignatureDeserializer</b> just owns the lifetime of the memory for the deserialized data structure.
      

The <b>REFIID</b>, or <b>GUID</b>, of the interface to the root signature deserializer can be obtained by using the __uuidof() macro. For example, __uuidof(<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer">ID3D12RootSignatureDeserializer</a>) will get the <b>GUID</b> of the interface to a root signature deserializer.
      

The function signature PFN_D3D12_CREATE_ROOT_SIGNATURE_DESERIALIZER is provided as a typedef, so that you can use dynamic linking techniques (<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a>) instead of statically linking.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-functions">Core Functions</a>



<a href="/windows/desktop/direct3d12/creating-a-root-signature">Creating a Root Signature</a>