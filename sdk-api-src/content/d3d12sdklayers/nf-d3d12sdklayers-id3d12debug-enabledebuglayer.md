---
UID: NF:d3d12sdklayers.ID3D12Debug.EnableDebugLayer
title: ID3D12Debug::EnableDebugLayer (d3d12sdklayers.h)
description: Enables the debug layer.
helpviewer_keywords: ["EnableDebugLayer","EnableDebugLayer method","EnableDebugLayer method","ID3D12Debug interface","ID3D12Debug interface","EnableDebugLayer method","ID3D12Debug.EnableDebugLayer","ID3D12Debug::EnableDebugLayer","d3d12sdklayers/ID3D12Debug::EnableDebugLayer","direct3d12.id3d12debug_enabledebuglayer"]
old-location: direct3d12\id3d12debug_enabledebuglayer.htm
tech.root: direct3d12
ms.assetid: 4C30C7C6-6071-4D69-BAB9-4CF6FED5B7D4
ms.date: 12/05/2018
ms.keywords: EnableDebugLayer, EnableDebugLayer method, EnableDebugLayer method,ID3D12Debug interface, ID3D12Debug interface,EnableDebugLayer method, ID3D12Debug.EnableDebugLayer, ID3D12Debug::EnableDebugLayer, d3d12sdklayers/ID3D12Debug::EnableDebugLayer, direct3d12.id3d12debug_enabledebuglayer
f1_keywords:
- d3d12sdklayers/ID3D12Debug.EnableDebugLayer
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
- ID3D12Debug.EnableDebugLayer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12Debug::EnableDebugLayer


## -description


Enables the debug layer.
        


## -parameters






## -remarks



To enable the debug layers using this API, it must be called before the D3D12 device is created. Calling this API after creating the D3D12 device will cause the D3D12 runtime to remove the device.


#### Examples

 Enable the D3D12 debug layer.

<pre class="syntax" xml:space="preserve"><code>// Enable the D3D12 debug layer.
{
    ComPtr&lt;ID3D12Debug&gt; debugController;
    if (SUCCEEDED(D3D12GetDebugInterface(IID_PPV_ARGS(&amp;debugController))))
    {
        debugController-&gt;EnableDebugLayer();
    }
}</code></pre>
Refer to the <a href="https://docs.microsoft.com/windows/desktop/direct3d12/notes-on-example-code">Example Code in the D3D12 Reference</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug">ID3D12Debug</a>
 

 

