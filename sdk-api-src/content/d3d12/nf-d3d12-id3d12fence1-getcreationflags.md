---
UID: NF:d3d12.ID3D12Fence1.GetCreationFlags
title: ID3D12Fence1::GetCreationFlags (d3d12.h)
description: Gets the flags used to create the fence represented by the current instance.
helpviewer_keywords: ["GetCreationFlags","GetCreationFlags method","GetCreationFlags method","ID3D12fence1 interface","ID3D12Fence1.GetCreationFlags","ID3D12Fence1::GetCreationFlags","ID3D12fence1 interface","GetCreationFlags method","ID3D12fence1::GetCreationFlags","d3d12/ID3D12fence1::GetCreationFlags","direct3d12.id3d12fence1_getcreationflags"]
old-location: direct3d12\id3d12fence1_getcreationflags.htm
tech.root: direct3d12
ms.assetid: 59FF0D7D-CE1F-49AD-8AFE-8C0E7DE05F36
ms.date: 12/05/2018
ms.keywords: GetCreationFlags, GetCreationFlags method, GetCreationFlags method,ID3D12fence1 interface, ID3D12Fence1.GetCreationFlags, ID3D12Fence1::GetCreationFlags, ID3D12fence1 interface,GetCreationFlags method, ID3D12fence1::GetCreationFlags, d3d12/ID3D12fence1::GetCreationFlags, direct3d12.id3d12fence1_getcreationflags
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
 - ID3D12Fence1::GetCreationFlags
 - d3d12/ID3D12Fence1::GetCreationFlags
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
 - ID3D12fence1.GetCreationFlags
---

# ID3D12Fence1::GetCreationFlags


## -description

Gets the flags used to create the fence represented by the current instance.



## -returns

Type: <b><a href="/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags">D3D12_FENCE_FLAGS</a></b>

The flags used to create the fence.

## -remarks

The flags returned by <b>GetCreationFlags</b> are used mainly for opening a shared fence.

## -see-also

<a href="/windows/win32/api/d3d12/nn-d3d12-id3d12fence1">Id3d12fence1</a>



<a href="/windows/win32/direct3d12/user-mode-heap-synchronization">Multi-engine synchronization</a>

