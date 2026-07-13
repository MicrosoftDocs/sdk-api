---
UID: NN:d3d12.ID3D12Fence1
title: ID3D12Fence1 (d3d12.h)
description: Represents a fence. This interface extends ID3D12Fence, and supports the retrieval of the flags used to create the original fence.
helpviewer_keywords: ["ID3D12Fence1","ID3D12Fence1 interface","ID3D12Fence1 interface","described","d3d12/ID3D12Fence1","direct3d12.id3d12fence1"]
old-location: direct3d12\id3d12fence1.htm
tech.root: direct3d12
ms.assetid: 292FA25B-7C72-4092-8822-DB15951A8309
ms.date: 12/05/2018
ms.keywords: ID3D12Fence1, ID3D12Fence1 interface, ID3D12Fence1 interface,described, d3d12/ID3D12Fence1, direct3d12.id3d12fence1
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
 - ID3D12Fence1
 - d3d12/ID3D12Fence1
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
 - ID3D12Fence1
---

# ID3D12Fence1 interface


## -description

Represents a fence. This interface extends <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a>, and supports the retrieval of the flags used to create the original fence.  This new feature is useful primarily for opening shared fences.
<div class="alert"><b>Note</b>  <b>ID3D12Fence1</b> was introduced in the Windows 10 Fall Creators Update, and is the latest version of the <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a> interface. Applications targeting Windows 10 Fall Creators Update and later should use <b>ID3D12Fence1</b> instead of earlier versions.</div><div> </div>

## -inheritance

The <b>ID3D12Fence1</b> interface inherits from <a href="/windows/win32/api/d3d12/nn-d3d12-id3d12fence">ID3D12Fence</a>. <b>ID3D12Fence1</b> also has these types of members:

## -see-also

<a href="/windows/win32/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="/windows/win32/direct3d12/fence-based-resource-management">Fence Based Resource Management</a>



<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12fence">ID3D12fence</a>



<a href="/windows/win32/direct3d12/user-mode-heap-synchronization">Multi-engine synchronization</a>

