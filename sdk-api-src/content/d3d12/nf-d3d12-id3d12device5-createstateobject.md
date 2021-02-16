---
UID: NF:d3d12.ID3D12Device5.CreateStateObject
title: ID3D12Device5::CreateStateObject (d3d12.h)
description: Creates an [ID3D12StateObject](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject).
helpviewer_keywords: ["CreateStateObject","CreateStateObject method","CreateStateObject method","ID3D12Device5 interface","ID3D12Device5 interface","CreateStateObject method","ID3D12Device5.CreateStateObject","ID3D12Device5::CreateStateObject","d3d12/ID3D12Device5::CreateStateObject","direct3d12.id3d12device5_createstateobject"]
old-location: direct3d12\id3d12device5_createstateobject.htm
tech.root: direct3d12
ms.assetid: 9CC759D5-6414-4B05-B8F3-FA6056A0A9AF
ms.date: 12/05/2018
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - ID3D12Device5::CreateStateObject
 - d3d12/ID3D12Device5::CreateStateObject
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
 - ID3D12Device5.CreateStateObject
---

## -description

Creates an [ID3D12StateObject](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject).

## -parameters

### -param pDesc [in]

The description of the state object to create.

### -param riid

The GUID of the interface to create. Use <i>__uuidof(ID3D12StateObject)</i>.

### -param ppStateObject [out]

The returned state object.

## -returns

Returns S_OK if successful; otherwise, returns one of the following values:

<ul>
<li>E_INVALIDARG if one of the input parameters is invalid.</li>
<li>E_OUTOFMEMORY if sufficient memory is not available to create the handle.</li>
<li>Possibly other error codes that are described in the <a href="/windows/desktop/direct3d12/d3d12-graphics-reference-returnvalues">Direct3D 12 Return Codes</a> topic.
              </li>
</ul>

## -see-also

[ID3D12Device5](/windows/win32/api/d3d12/nn-d3d12-id3d12device5)
