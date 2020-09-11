---
UID: NN:d3d12.ID3D12GraphicsCommandList2
title: ID3D12GraphicsCommandList2 (d3d12.h)
description: Encapsulates a list of graphics commands for rendering, extending the interface to support writing immediate values directly to a buffer.
helpviewer_keywords: ["ID3D12GraphicsCommandList2","ID3D12GraphicsCommandList2 interface","ID3D12GraphicsCommandList2 interface","described","d3d12/ID3D12GraphicsCommandList2","direct3d12.id3d12graphicscommandlist2"]
old-location: direct3d12\id3d12graphicscommandlist2.htm
tech.root: direct3d12
ms.assetid: 6A1BF079-CAE7-45E9-A95F-E19ACD380143
ms.date: 12/05/2018
ms.keywords: ID3D12GraphicsCommandList2, ID3D12GraphicsCommandList2 interface, ID3D12GraphicsCommandList2 interface,described, d3d12/ID3D12GraphicsCommandList2, direct3d12.id3d12graphicscommandlist2
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
 - ID3D12GraphicsCommandList2
 - d3d12/ID3D12GraphicsCommandList2
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
 - ID3D12GraphicsCommandList2
---

# ID3D12GraphicsCommandList2 interface


## -description

Encapsulates a list of graphics commands for rendering, extending the interface to support writing immediate values directly to a buffer.
<div class="alert"><b>Note</b>  This interface was introduced in the Windows 10 Fall Creators Update, and  as such is the latest version of the <b>ID3D12GraphicsCommandList</b> interface. Applications targeting the Windows 10 Fall Creators Update and later should use this interface instead of <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist1">ID3D12GraphicsCommandList1</a> or <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12GraphicsCommandList2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist1">ID3D12GraphicsCommandList1</a>. <b>ID3D12GraphicsCommandList2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12GraphicsCommandList2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist2-writebufferimmediate">WriteBufferImmediate</a>
</td>
<td align="left" width="63%">
Writes a number of 32-bit immediate values to the specified buffer locations directly from the command stream.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist">ID3D12GraphicsCommandList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist1">ID3D12GraphicsCommandList1</a>

