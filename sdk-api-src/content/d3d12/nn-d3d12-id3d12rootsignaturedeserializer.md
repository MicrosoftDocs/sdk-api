---
UID: NN:d3d12.ID3D12RootSignatureDeserializer
title: ID3D12RootSignatureDeserializer (d3d12.h)
description: Contains a method to return the deserialized D3D12_ROOT_SIGNATURE_DESC data structure, of a serialized root signature version 1.0.
helpviewer_keywords: ["ID3D12RootSignatureDeserializer","ID3D12RootSignatureDeserializer interface","ID3D12RootSignatureDeserializer interface","described","d3d12/ID3D12RootSignatureDeserializer","direct3d12.id3d12rootsignaturedeserializer"]
old-location: direct3d12\id3d12rootsignaturedeserializer.htm
tech.root: direct3d12
ms.assetid: FEDA0802-45A6-4ED5-9683-5278BD60B7A4
ms.date: 12/05/2018
ms.keywords: ID3D12RootSignatureDeserializer, ID3D12RootSignatureDeserializer interface, ID3D12RootSignatureDeserializer interface,described, d3d12/ID3D12RootSignatureDeserializer, direct3d12.id3d12rootsignaturedeserializer
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
 - ID3D12RootSignatureDeserializer
 - d3d12/ID3D12RootSignatureDeserializer
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
 - ID3D12RootSignatureDeserializer
---

# ID3D12RootSignatureDeserializer interface


## -description

Contains a method to  return the deserialized 
          <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc">D3D12_ROOT_SIGNATURE_DESC</a> 
          data structure, of a serialized root signature version 1.0.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12RootSignatureDeserializer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12RootSignatureDeserializer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12RootSignatureDeserializer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12rootsignaturedeserializer-getrootsignaturedesc">GetRootSignatureDesc</a>
</td>
<td align="left" width="63%">
Gets the layout of the root signature.
        

</td>
</tr>
</table>

## -remarks

This interface has been superceded by <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer">ID3D12VersionedRootSignatureDeserializer</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/direct3d12/root-signatures">Root Signatures</a>