---
UID: NN:d3d11_3.ID3D11DeviceContext4
title: ID3D11DeviceContext4 (d3d11_3.h)
description: The device context interface represents a device context; it is used to render commands. ID3D11DeviceContext4 adds new methods to those in ID3D11DeviceContext3.
helpviewer_keywords: ["ID3D11DeviceContext4","ID3D11DeviceContext4 interface [Direct3D 11]","ID3D11DeviceContext4 interface [Direct3D 11]","described","d3d11_3/ID3D11DeviceContext4","direct3d11.id3d11devicecontext4"]
old-location: direct3d11\id3d11devicecontext4.htm
tech.root: direct3d11
ms.assetid: 9A4B737C-C0A8-4319-A9CA-8172E992774D
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext4, ID3D11DeviceContext4 interface [Direct3D 11], ID3D11DeviceContext4 interface [Direct3D 11],described, d3d11_3/ID3D11DeviceContext4, direct3d11.id3d11devicecontext4
f1_keywords:
- d3d11_3/ID3D11DeviceContext4
dev_langs:
- c++
req.header: d3d11_3.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D11.lib
- D3D11.dll
api_name:
- ID3D11DeviceContext4
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11DeviceContext4 interface


## -description


The device context interface represents a device context; it is used to render commands. <b>ID3D11DeviceContext4</b> adds new methods to those in <a href="https://docs.microsoft.com/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3">ID3D11DeviceContext3</a>.
<div class="alert"><b>Note</b>  This interface, introduced in the Windows 10 Creators Update, is the latest version of the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> interface. Applications targetting Windows 10 Creators Update should use this interface instead of earlier versions.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11DeviceContext4</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3">ID3D11DeviceContext3</a>. <b>ID3D11DeviceContext4</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11DeviceContext4</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11devicecontext4-signal">Signal</a>
</td>
<td align="left" width="63%">
Updates a fence to a specified value after all previous work has completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11devicecontext4-wait">Wait</a>
</td>
<td align="left" width="63%">
Waits until the specified fence reaches or exceeds the specified value before future work can begin.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2">ID3D11DeviceContect2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1">ID3D11DeviceContext1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_3/nn-d3d11_3-id3d11devicecontext3">ID3D11DeviceContext3</a>
 

 

