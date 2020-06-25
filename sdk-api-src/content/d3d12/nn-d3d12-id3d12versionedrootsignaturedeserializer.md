---
UID: NN:d3d12.ID3D12VersionedRootSignatureDeserializer
title: ID3D12VersionedRootSignatureDeserializer (d3d12.h)
description: Contains methods to return the deserialized D3D12_ROOT_SIGNATURE_DESC1 data structure, of any version of a serialized root signature.
helpviewer_keywords: ["ID3D12VersionedRootSignatureDeserializer","ID3D12VersionedRootSignatureDeserializer interface","ID3D12VersionedRootSignatureDeserializer interface","described","d3d12/ID3D12VersionedRootSignatureDeserializer","direct3d12.id3d12versionedrootsignaturedeserializer"]
old-location: direct3d12\id3d12versionedrootsignaturedeserializer.htm
tech.root: direct3d12
ms.assetid: 3B1E9837-72CA-4C44-B06C-C77E32480958
ms.date: 12/05/2018
ms.keywords: ID3D12VersionedRootSignatureDeserializer, ID3D12VersionedRootSignatureDeserializer interface, ID3D12VersionedRootSignatureDeserializer interface,described, d3d12/ID3D12VersionedRootSignatureDeserializer, direct3d12.id3d12versionedrootsignaturedeserializer
f1_keywords:
- d3d12/ID3D12VersionedRootSignatureDeserializer
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- d3d12.dll
api_name:
- ID3D12VersionedRootSignatureDeserializer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12VersionedRootSignatureDeserializer interface


## -description


Contains methods to  return the deserialized 
          <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc1">D3D12_ROOT_SIGNATURE_DESC1</a> 
          data structure, of any version of a serialized root signature.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12VersionedRootSignatureDeserializer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12VersionedRootSignatureDeserializer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12VersionedRootSignatureDeserializer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getrootsignaturedescatversion">GetRootSignatureDescAtVersion</a>
</td>
<td align="left" width="63%">
Converts root signature description structures to a requested version.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc">GetUnconvertedRootSignatureDesc</a>
</td>
<td align="left" width="63%">
Gets the layout of the root signature, without converting between root signature versions.
        

</td>
</tr>
</table> 


## -remarks



This interface supercedes <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer">ID3D12RootSignatureDeserializer</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d12/root-signature-version-1-1">Root Signature Version 1.1</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d12/root-signatures">Root Signatures</a>
 

 

