---
UID: NN:d3d12.ID3D12VersionedRootSignatureDeserializer
title: ID3D12VersionedRootSignatureDeserializer
author: windows-driver-content
description: Contains methods to return the deserialized D3D12_ROOT_SIGNATURE_DESC1 data structure, of any version of a serialized root signature.
old-location: direct3d12\id3d12versionedrootsignaturedeserializer.htm
old-project: direct3d12
ms.assetid: 3B1E9837-72CA-4C44-B06C-C77E32480958
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ID3D12VersionedRootSignatureDeserializer, ID3D12VersionedRootSignatureDeserializer interface, ID3D12VersionedRootSignatureDeserializer interface, described, d3d12/ID3D12VersionedRootSignatureDeserializer, direct3d12.id3d12versionedrootsignaturedeserializer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: D3D_SHADER_MODEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d12.dll
api_name:
-	ID3D12VersionedRootSignatureDeserializer
product: Windows
targetos: Windows
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
---

# ID3D12VersionedRootSignatureDeserializer interface


## -description


Contains methods to  return the deserialized 
          <a href="https://msdn.microsoft.com/F085D077-1DA8-41A1-9FA3-4423EA003345">D3D12_ROOT_SIGNATURE_DESC1</a> 
          data structure, of any version of a serialized root signature.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12VersionedRootSignatureDeserializer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D12VersionedRootSignatureDeserializer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/50EB9AC8-D13D-41D3-9E16-AC9871095A72">GetRootSignatureDescAtVersion</a>
</td>
<td align="left" width="63%">
Converts root signature description structures to a requested version.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7E21B598-C13B-4418-B5B1-4ADDAA18F9B9">GetUnconvertedRootSignatureDesc</a>
</td>
<td align="left" width="63%">

          Gets the layout of the root signature, without converting between root signature versions.
        

</td>
</tr>
</table> 


## -remarks



This interface supercedes <a href="https://msdn.microsoft.com/FEDA0802-45A6-4ED5-9683-5278BD60B7A4">ID3D12RootSignatureDeserializer</a>.




## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/8FE42C1C-7F1D-4E70-A7EE-D5EC67237327">Root Signature Version 1.1</a>



<a href="https://msdn.microsoft.com/EE32A222-8469-4AF5-B688-AFA70CF77C6A">Root Signatures</a>
 

 

