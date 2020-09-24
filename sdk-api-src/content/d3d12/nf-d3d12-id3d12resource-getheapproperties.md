---
UID: NF:d3d12.ID3D12Resource.GetHeapProperties
title: ID3D12Resource::GetHeapProperties (d3d12.h)
description: Retrieves the properties of the resource heap, for placed and committed resources.
helpviewer_keywords: ["GetHeapProperties","GetHeapProperties method","GetHeapProperties method","ID3D12Resource interface","ID3D12Resource interface","GetHeapProperties method","ID3D12Resource.GetHeapProperties","ID3D12Resource::GetHeapProperties","d3d12/ID3D12Resource::GetHeapProperties","direct3d12.id3d12resource_getheapproperties"]
old-location: direct3d12\id3d12resource_getheapproperties.htm
tech.root: direct3d12
ms.assetid: 7F76986D-02F1-4E5A-B9A4-CFB021B72026
ms.date: 12/05/2018
ms.keywords: GetHeapProperties, GetHeapProperties method, GetHeapProperties method,ID3D12Resource interface, ID3D12Resource interface,GetHeapProperties method, ID3D12Resource.GetHeapProperties, ID3D12Resource::GetHeapProperties, d3d12/ID3D12Resource::GetHeapProperties, direct3d12.id3d12resource_getheapproperties
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
 - ID3D12Resource::GetHeapProperties
 - d3d12/ID3D12Resource::GetHeapProperties
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
 - ID3D12Resource.GetHeapProperties
---

# ID3D12Resource::GetHeapProperties


## -description

Retrieves the properties of the resource heap, for placed and committed resources.

## -parameters

### -param pHeapProperties [out, optional]

Type: <b><a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties">D3D12_HEAP_PROPERTIES</a>*</b>

Pointer to a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_heap_properties">D3D12_HEAP_PROPERTIES</a> structure, that on successful completion of the method will contain the resource heap properties.

### -param pHeapFlags [out, optional]

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags">D3D12_HEAP_FLAGS</a>*</b>

Specifies a <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_heap_flags">D3D12_HEAP_FLAGS</a> variable, that on successful completion of the method will contain any miscellaneous heap flags.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a>.
            If the resource was created as reserved, E_INVALIDARG is returned.

## -remarks

This method only works on placed and committed resources, not on reserved resources.
          If the resource was created as reserved, E_INVALIDARG is returned.
          The pages could be mapped to none, one, or more heaps.
        

For more information, refer to <a href="/windows/desktop/direct3d12/memory-management">Memory Management in Direct3D 12</a>.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12resource">ID3D12Resource</a>