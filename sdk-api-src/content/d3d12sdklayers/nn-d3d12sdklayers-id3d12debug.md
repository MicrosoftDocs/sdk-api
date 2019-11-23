---
UID: NN:d3d12sdklayers.ID3D12Debug
title: ID3D12Debug (d3d12sdklayers.h)

description: A debug interface controls debug settings and validates pipeline state. It can only be used if the debug layer is turned on.
old-location: direct3d12\id3d12debug.htm
tech.root: direct3d12
ms.assetid: 6CFAE096-EE09-4DD0-ADA3-A700FD9FDCB9

ms.date: 12/05/2018
ms.keywords: ID3D12Debug, ID3D12Debug interface, ID3D12Debug interface,described, d3d12sdklayers/ID3D12Debug, direct3d12.id3d12debug
ms.topic: interface
f1_keywords: 
 - "d3d12sdklayers/ID3D12Debug"
dev_langs:
 - c++
req.header: d3d12sdklayers.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12Debug
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12Debug interface


## -description


A debug interface controls debug settings and validates pipeline state. It can only be used if the debug layer is turned on.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Debug</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12Debug</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12Debug</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug-enabledebuglayer">EnableDebugLayer</a>
</td>
<td align="left" width="63%">
Enables the debug layer.
        

</td>
</tr>
</table> 


## -remarks



This interface is obtained by querying it from the <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nn-d3d12-id3d12device">ID3D12Device</a> using <code>IUnknown::QueryInterface</code>. 

 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-sdklayers-interfaces">Debug Layer Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

