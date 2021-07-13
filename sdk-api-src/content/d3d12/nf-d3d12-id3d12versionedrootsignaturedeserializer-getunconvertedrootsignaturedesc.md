---
UID: NF:d3d12.ID3D12VersionedRootSignatureDeserializer.GetUnconvertedRootSignatureDesc
title: ID3D12VersionedRootSignatureDeserializer::GetUnconvertedRootSignatureDesc (d3d12.h)
description: Gets the layout of the root signature, without converting between root signature versions.
helpviewer_keywords: ["GetUnconvertedRootSignatureDesc","GetUnconvertedRootSignatureDesc method","GetUnconvertedRootSignatureDesc method","ID3D12VersionedRootSignatureDeserializer interface","ID3D12VersionedRootSignatureDeserializer interface","GetUnconvertedRootSignatureDesc method","ID3D12VersionedRootSignatureDeserializer.GetUnconvertedRootSignatureDesc","ID3D12VersionedRootSignatureDeserializer::GetUnconvertedRootSignatureDesc","d3d12/ID3D12VersionedRootSignatureDeserializer::GetUnconvertedRootSignatureDesc","direct3d12.id3d12versionedrootsignaturedeserializer_getunconvertedrootsignaturedesc"]
old-location: direct3d12\id3d12versionedrootsignaturedeserializer_getunconvertedrootsignaturedesc.htm
tech.root: direct3d12
ms.assetid: 7E21B598-C13B-4418-B5B1-4ADDAA18F9B9
ms.date: 12/05/2018
ms.keywords: GetUnconvertedRootSignatureDesc, GetUnconvertedRootSignatureDesc method, GetUnconvertedRootSignatureDesc method,ID3D12VersionedRootSignatureDeserializer interface, ID3D12VersionedRootSignatureDeserializer interface,GetUnconvertedRootSignatureDesc method, ID3D12VersionedRootSignatureDeserializer.GetUnconvertedRootSignatureDesc, ID3D12VersionedRootSignatureDeserializer::GetUnconvertedRootSignatureDesc, d3d12/ID3D12VersionedRootSignatureDeserializer::GetUnconvertedRootSignatureDesc, direct3d12.id3d12versionedrootsignaturedeserializer_getunconvertedrootsignaturedesc
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
 - ID3D12VersionedRootSignatureDeserializer::GetUnconvertedRootSignatureDesc
 - d3d12/ID3D12VersionedRootSignatureDeserializer::GetUnconvertedRootSignatureDesc
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
 - ID3D12VersionedRootSignatureDeserializer.GetUnconvertedRootSignatureDesc
---

# ID3D12VersionedRootSignatureDeserializer::GetUnconvertedRootSignatureDesc


## -description

Gets the layout of the root signature, without converting between root signature versions.



## -returns

Type: <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc">D3D12_VERSIONED_ROOT_SIGNATURE_DESC</a></b>

This method returns a deserialized root signature in a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc">D3D12_VERSIONED_ROOT_SIGNATURE_DESC</a> structure that describes the layout of the root signature.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer">ID3D12VersionedRootSignatureDeserializer</a>



<a href="/windows/desktop/direct3d12/root-signature-version-1-1">Root Signature Version 1.1</a>
