---
UID: NF:d3d11.ID3D11CommandList.GetContextFlags
title: ID3D11CommandList::GetContextFlags (d3d11.h)
description: Gets the initialization flags associated with the deferred context that created the command list.
helpviewer_keywords: ["64bf9914-05c2-c831-c3c4-d1181d8ca907","GetContextFlags","GetContextFlags method [Direct3D 11]","GetContextFlags method [Direct3D 11]","ID3D11CommandList interface","ID3D11CommandList interface [Direct3D 11]","GetContextFlags method","ID3D11CommandList.GetContextFlags","ID3D11CommandList::GetContextFlags","d3d11/ID3D11CommandList::GetContextFlags","direct3d11.id3d11commandlist_getcontextflags"]
old-location: direct3d11\id3d11commandlist_getcontextflags.htm
tech.root: direct3d11
ms.assetid: a3d98f3f-6e66-408e-baee-661afb65c0a4
ms.date: 12/05/2018
ms.keywords: 64bf9914-05c2-c831-c3c4-d1181d8ca907, GetContextFlags, GetContextFlags method [Direct3D 11], GetContextFlags method [Direct3D 11],ID3D11CommandList interface, ID3D11CommandList interface [Direct3D 11],GetContextFlags method, ID3D11CommandList.GetContextFlags, ID3D11CommandList::GetContextFlags, d3d11/ID3D11CommandList::GetContextFlags, direct3d11.id3d11commandlist_getcontextflags
req.header: d3d11.h
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
req.lib: D3d11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11CommandList::GetContextFlags
 - d3d11/ID3D11CommandList::GetContextFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.lib
 - d3d11.dll
api_name:
 - ID3D11CommandList.GetContextFlags
---

# ID3D11CommandList::GetContextFlags


## -description

Gets the initialization flags associated with the deferred context that created the command list.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The context flag is reserved for future use and is always 0.

## -remarks

The GetContextFlags method gets the flags that were supplied to the <i>ContextFlags</i> parameter of <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createdeferredcontext">ID3D11Device::CreateDeferredContext</a>; however, the context flag is reserved for future use.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11commandlist">ID3D11CommandList</a>
