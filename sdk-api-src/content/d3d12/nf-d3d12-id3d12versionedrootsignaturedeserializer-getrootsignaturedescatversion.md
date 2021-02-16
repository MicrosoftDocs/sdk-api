---
UID: NF:d3d12.ID3D12VersionedRootSignatureDeserializer.GetRootSignatureDescAtVersion
title: ID3D12VersionedRootSignatureDeserializer::GetRootSignatureDescAtVersion (d3d12.h)
description: Converts root signature description structures to a requested version.
helpviewer_keywords: ["GetRootSignatureDescAtVersion","GetRootSignatureDescAtVersion method","GetRootSignatureDescAtVersion method","ID3D12VersionedRootSignatureDeserializer interface","ID3D12VersionedRootSignatureDeserializer interface","GetRootSignatureDescAtVersion method","ID3D12VersionedRootSignatureDeserializer.GetRootSignatureDescAtVersion","ID3D12VersionedRootSignatureDeserializer::GetRootSignatureDescAtVersion","d3d12/ID3D12VersionedRootSignatureDeserializer::GetRootSignatureDescAtVersion","direct3d12.id3d12versionedrootsignaturedeserializer_getrootsignaturedescatversion"]
old-location: direct3d12\id3d12versionedrootsignaturedeserializer_getrootsignaturedescatversion.htm
tech.root: direct3d12
ms.assetid: 50EB9AC8-D13D-41D3-9E16-AC9871095A72
ms.date: 12/05/2018
ms.keywords: GetRootSignatureDescAtVersion, GetRootSignatureDescAtVersion method, GetRootSignatureDescAtVersion method,ID3D12VersionedRootSignatureDeserializer interface, ID3D12VersionedRootSignatureDeserializer interface,GetRootSignatureDescAtVersion method, ID3D12VersionedRootSignatureDeserializer.GetRootSignatureDescAtVersion, ID3D12VersionedRootSignatureDeserializer::GetRootSignatureDescAtVersion, d3d12/ID3D12VersionedRootSignatureDeserializer::GetRootSignatureDescAtVersion, direct3d12.id3d12versionedrootsignaturedeserializer_getrootsignaturedescatversion
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
 - ID3D12VersionedRootSignatureDeserializer::GetRootSignatureDescAtVersion
 - d3d12/ID3D12VersionedRootSignatureDeserializer::GetRootSignatureDescAtVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VersionedRootSignatureDeserializer.GetRootSignatureDescAtVersion
---

# ID3D12VersionedRootSignatureDeserializer::GetRootSignatureDescAtVersion


## -description

Converts root signature description structures to a requested version.

## -parameters

### -param convertToVersion

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version">D3D_ROOT_SIGNATURE_VERSION</a></b>

Specifies the required <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version">D3D_ROOT_SIGNATURE_VERSION</a>.

### -param ppDesc [out]

Type: <b>const <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc">D3D12_VERSIONED_ROOT_SIGNATURE_DESC</a>**</b>

Contains the deserialized root signature in a  <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc">D3D12_VERSIONED_ROOT_SIGNATURE_DESC</a> structure.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code. The method can fail with E_OUTOFMEMORY.

## -remarks

This method allocates additional storage if needed for the converted root signature (memory owned by the deserializer interface).  If conversion is done, the deserializer interface doesn’t free the original deserialized root signature memory – all versions the interface has been asked to convert to are available until the deserializer is destroyed. 

Converting a root signature from 1.1 to 1.0 will drop all <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_descriptor_range_flags">D3D12_DESCRIPTOR_RANGE_FLAGS</a> and <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags">D3D12_ROOT_DESCRIPTOR_FLAGS</a> can be useful for generating compatible root signatures that need to run on old operating systems, though does lose optimization opportunities.  For instance, multiple root signature versions can be serialized and stored with application assets, with the appropriate version used at runtime based on the operating system capabilities.  

Converting a root signature from 1.0 to 1.1 just adds the appropriate flags to match 1.0 semantics.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer">ID3D12VersionedRootSignatureDeserializer</a>



<a href="/windows/desktop/direct3d12/root-signature-version-1-1">Root Signature Version 1.1</a>