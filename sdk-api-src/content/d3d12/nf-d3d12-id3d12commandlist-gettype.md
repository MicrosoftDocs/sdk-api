---
UID: NF:d3d12.ID3D12CommandList.GetType
title: ID3D12CommandList::GetType (d3d12.h)
description: Gets the type of the command list, such as direct, bundle, compute, or copy.
helpviewer_keywords: ["GetType","GetType method","GetType method","ID3D12CommandList interface","ID3D12CommandList interface","GetType method","ID3D12CommandList.GetType","ID3D12CommandList::GetType","d3d12/ID3D12CommandList::GetType","direct3d12.id3d12commandlist_gettype"]
old-location: direct3d12\id3d12commandlist_gettype.htm
tech.root: direct3d12
ms.assetid: 39F9EF96-9761-410A-B5DD-A088F6863923
ms.date: 12/05/2018
ms.keywords: GetType, GetType method, GetType method,ID3D12CommandList interface, ID3D12CommandList interface,GetType method, ID3D12CommandList.GetType, ID3D12CommandList::GetType, d3d12/ID3D12CommandList::GetType, direct3d12.id3d12commandlist_gettype
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
 - ID3D12CommandList::GetType
 - d3d12/ID3D12CommandList::GetType
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
 - ID3D12CommandList.GetType
---

# ID3D12CommandList::GetType


## -description

Gets the type of the command list, such as direct, bundle, compute, or copy.



## -returns

Type: <b><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type">D3D12_COMMAND_LIST_TYPE</a></b>

This method returns the type of the command list, 
            as a <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type">D3D12_COMMAND_LIST_TYPE</a> enumeration constant, 
            such as direct, bundle, compute, or copy.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist">ID3D12CommandList</a>
