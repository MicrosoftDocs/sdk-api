---
UID: NN:d3dcsx.ID3DX11Scan
title: ID3DX11Scan (d3dcsx.h)
description: Scan context.
helpviewer_keywords: ["ID3DX11Scan","ID3DX11Scan interface [Direct3D 11]","ID3DX11Scan interface [Direct3D 11]","described","d3dcsx/ID3DX11Scan","direct3d11.id3dx11scan","f606bccf-3795-f179-4742-0c561a907373"]
old-location: direct3d11\id3dx11scan.htm
tech.root: direct3d11
ms.assetid: f57401b9-fa1e-4470-a974-825749773f95
ms.date: 12/05/2018
ms.keywords: ID3DX11Scan, ID3DX11Scan interface [Direct3D 11], ID3DX11Scan interface [Direct3D 11],described, d3dcsx/ID3DX11Scan, direct3d11.id3dx11scan, f606bccf-3795-f179-4742-0c561a907373
req.header: d3dcsx.h
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
req.lib: D3dcsx.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3DX11Scan
 - d3dcsx/ID3DX11Scan
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3dcsx.lib
 - d3dcsx.dll
api_name:
 - ID3DX11Scan
---

# ID3DX11Scan interface


## -description

Scan context.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3DX11Scan</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3DX11Scan</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3DX11Scan</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-id3dx11scan-multiscan">Multiscan</a>
</td>
<td align="left" width="63%">
Performs a multiscan of a sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-id3dx11scan-scan">Scan</a>
</td>
<td align="left" width="63%">
Performs an unsegmented scan of a sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-id3dx11scan-setscandirection">SetScanDirection</a>
</td>
<td align="left" width="63%">
Sets which direction to perform scans in.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3dcsx11-interfaces">D3DCSX 11 Interfaces</a>