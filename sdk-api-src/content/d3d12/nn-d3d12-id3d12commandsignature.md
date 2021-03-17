---
UID: NN:d3d12.ID3D12CommandSignature
title: ID3D12CommandSignature (d3d12.h)
description: A command signature object enables apps to specify indirect drawing, including the buffer format, command type and resource bindings to be used.
helpviewer_keywords: ["ID3D12CommandSignature","ID3D12CommandSignature interface","ID3D12CommandSignature interface","described","d3d12/ID3D12CommandSignature","direct3d12.id3d12commandsignature"]
old-location: direct3d12\id3d12commandsignature.htm
tech.root: direct3d12
ms.assetid: 57EC15D0-9056-4AFC-86EF-3658DEA8AF40
ms.date: 12/05/2018
ms.keywords: ID3D12CommandSignature, ID3D12CommandSignature interface, ID3D12CommandSignature interface,described, d3d12/ID3D12CommandSignature, direct3d12.id3d12commandsignature
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
 - ID3D12CommandSignature
 - d3d12/ID3D12CommandSignature
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
 - ID3D12CommandSignature
---

# ID3D12CommandSignature interface


## -description

A command signature object enables apps to specify indirect drawing, including the buffer format, command type and resource bindings to be used.

## -remarks

To create a command signature, call <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandsignature">ID3D12Device::CreateCommandSignature</a>, as described in <a href="/windows/desktop/direct3d12/indirect-drawing">Indirect Drawing</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect">ExecuteIndirect</a>



<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a>