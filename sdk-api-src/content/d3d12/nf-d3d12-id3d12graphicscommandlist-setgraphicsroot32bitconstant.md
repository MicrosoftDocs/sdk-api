---
UID: NF:d3d12.ID3D12GraphicsCommandList.SetGraphicsRoot32BitConstant
title: ID3D12GraphicsCommandList::SetGraphicsRoot32BitConstant (d3d12.h)
description: Sets a constant in the graphics root signature.
helpviewer_keywords: ["ID3D12GraphicsCommandList interface","SetGraphicsRoot32BitConstant method","ID3D12GraphicsCommandList.SetGraphicsRoot32BitConstant","ID3D12GraphicsCommandList::SetGraphicsRoot32BitConstant","SetGraphicsRoot32BitConstant","SetGraphicsRoot32BitConstant method","SetGraphicsRoot32BitConstant method","ID3D12GraphicsCommandList interface","d3d12/ID3D12GraphicsCommandList::SetGraphicsRoot32BitConstant","direct3d12.id3d12graphicscommandlist_setgraphicsroot32bitconstant"]
old-location: direct3d12\id3d12graphicscommandlist_setgraphicsroot32bitconstant.htm
tech.root: direct3d12
ms.assetid: F53090CC-05E9-4892-B6BF-0A849A5D98EF
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList interface,SetGraphicsRoot32BitConstant method, ID3D12GraphicsCommandList.SetGraphicsRoot32BitConstant, ID3D12GraphicsCommandList::SetGraphicsRoot32BitConstant, SetGraphicsRoot32BitConstant, SetGraphicsRoot32BitConstant method, SetGraphicsRoot32BitConstant method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::SetGraphicsRoot32BitConstant, direct3d12.id3d12graphicscommandlist_setgraphicsroot32bitconstant
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
 - ID3D12GraphicsCommandList::SetGraphicsRoot32BitConstant
 - d3d12/ID3D12GraphicsCommandList::SetGraphicsRoot32BitConstant
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
 - ID3D12GraphicsCommandList.SetGraphicsRoot32BitConstant
---

# ID3D12GraphicsCommandList::SetGraphicsRoot32BitConstant


## -description

Sets a constant in the graphics root signature.

## -parameters

### -param RootParameterIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The slot number for binding.

### -param SrcData [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The source data for the constant to set.

### -param DestOffsetIn32BitValues [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The offset, in 32-bit values, to set the constant in the root signature.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>