---
UID: NN:d3d12sdklayers.ID3D12SharingContract
title: ID3D12SharingContract (d3d12sdklayers.h)
description: Part of a contract between D3D11On12 diagnostic layers and graphics diagnostics tools.
helpviewer_keywords: ["ID3D12SharingContract","ID3D12SharingContract interface","ID3D12SharingContract interface","described","d3d12sdklayers/ID3D12SharingContract","direct3d12.id3d12sharingcontract"]
old-location: direct3d12\id3d12sharingcontract.htm
tech.root: direct3d12
ms.assetid: 10E61C88-0CDC-42E6-AB70-4911D254C40A
ms.date: 12/05/2018
ms.keywords: ID3D12SharingContract, ID3D12SharingContract interface, ID3D12SharingContract interface,described, d3d12sdklayers/ID3D12SharingContract, direct3d12.id3d12sharingcontract
req.header: d3d12sdklayers.h
req.include-header: D3D12.h
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
 - ID3D12SharingContract
 - d3d12sdklayers/ID3D12SharingContract
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
 - ID3D12SharingContract
---

# ID3D12SharingContract interface


## -description

Part of a contract between D3D11On12 diagnostic layers and graphics diagnostics tools. This interface facilitates diagnostics tools to capture information at a lower level than the DXGI swapchain.

You may want to use this interface to enable diagnostic tools to capture usage patterns that don't use DXGI swap chains for presentation. If so, you can access this interface via **QueryInterface** from a D3D12 command queue. Note that this interface is not supported when there are no diagnostic tools present, so your application mustn't rely on it existing.

## -inheritance

The <b>ID3D12SharingContract</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12SharingContract</b> also has these types of members:

## -see-also

[Core interfaces](/windows/desktop/direct3d12/direct3d-12-interfaces), [IUnknown](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
