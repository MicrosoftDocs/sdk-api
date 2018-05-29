---
UID: NN:d3d12.ID3D12RootSignatureDeserializer
title: ID3D12RootSignatureDeserializer
author: windows-sdk-content
description: Contains a method to return the deserialized D3D12_ROOT_SIGNATURE_DESC data structure, of a serialized root signature version 1.0.
old-location: direct3d12\id3d12rootsignaturedeserializer.htm
old-project: direct3d12
ms.assetid: FEDA0802-45A6-4ED5-9683-5278BD60B7A4
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: ID3D12RootSignatureDeserializer, ID3D12RootSignatureDeserializer interface, ID3D12RootSignatureDeserializer interface,described, d3d12/ID3D12RootSignatureDeserializer, direct3d12.id3d12rootsignaturedeserializer
ms.prod: windows
ms.technology: windows-sdk
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
-	D3D12.dll
api_name:
-	ID3D12RootSignatureDeserializer
product: Windows
targetos: Windows
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
---

# ID3D12RootSignatureDeserializer interface


## -description


Contains a method to  return the deserialized 
          <a href="https://msdn.microsoft.com/D74D9D3B-96AB-489A-A91C-4F68AC3D05EE">D3D12_ROOT_SIGNATURE_DESC</a> 
          data structure, of a serialized root signature version 1.0.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12RootSignatureDeserializer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D12RootSignatureDeserializer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/A13FB848-A5C1-4B9B-9009-B0166A3A1C8D">GetRootSignatureDesc</a>
</td>
<td align="left" width="63%">

          Gets the layout of the root signature.
        

</td>
</tr>
</table> 


## -remarks



This interface has been superceded by <a href="https://msdn.microsoft.com/3B1E9837-72CA-4C44-B06C-C77E32480958">ID3D12VersionedRootSignatureDeserializer</a>.




## -see-also




<a href="https://msdn.microsoft.com/A9BD5910-8FF2-4540-BB8E-E8EA5C10528C">Core Interfaces</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/EE32A222-8469-4AF5-B688-AFA70CF77C6A">Root Signatures</a>
 

 

