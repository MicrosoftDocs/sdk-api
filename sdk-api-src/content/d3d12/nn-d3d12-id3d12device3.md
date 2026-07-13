---
UID: NN:d3d12.ID3D12Device3
title: ID3D12Device3 (d3d12.h)
description: Represents a virtual adapter. This interface extends ID3D12Device2 to support the creation of special-purpose diagnostic heaps in system memory that persist even in the event of a GPU-fault or device-removed scenario.
helpviewer_keywords: ["ID3D12Device3","ID3D12Device3 interface","ID3D12Device3 interface","described","d3d12/ID3D12Device3","direct3d12.id3d12device3"]
old-location: direct3d12\id3d12device3.htm
tech.root: direct3d12
ms.assetid: 038E546C-4000-401A-8A11-7A83F391676E
ms.date: 12/05/2018
ms.keywords: ID3D12Device3, ID3D12Device3 interface, ID3D12Device3 interface,described, d3d12/ID3D12Device3, direct3d12.id3d12device3
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
 - ID3D12Device3
 - d3d12/ID3D12Device3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3d12.dll
api_name:
 - ID3D12Device3
---

# ID3D12Device3 interface


## -description

Represents a virtual adapter. This interface extends <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device2">ID3D12Device2</a> to support the creation of special-purpose diagnostic heaps in system memory that persist even in the event of a GPU-fault or device-removed scenario.
<div class="alert"><b>Note</b>  This interface, introduced in the Windows 10 Fall Creators Update, is the latest version of the <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a> interface. Applications targeting the Windows 10 Fall Creators Update and later should use this interface instead of earlier versions.</div><div> </div>

## -inheritance

The <b>ID3D12Device3</b> interface inherits from <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device2">ID3D12Device2</a>. <b>ID3D12Device3</b> also has these types of members:

## -remarks

Use <a href="/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice">D3D12CreateDevice</a> to create a device.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device1">ID3D12Device1</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device2">ID3D12Device2</a>
