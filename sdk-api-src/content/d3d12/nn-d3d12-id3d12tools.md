---
UID: NN:d3d12.ID3D12Tools
title: ID3D12Tools (d3d12.h)
description: This interface is used to configure the runtime for tools such as PIX. Its not intended or supported for any other scenario.helpviewer_keywords: ["ID3D12Tools","ID3D12Tools interface","ID3D12Tools interface","described","d3d12/ID3D12Tools","direct3d12.id3d12tools"]
old-location: direct3d12\id3d12tools.htm
tech.root: direct3d12
ms.assetid: F192AC22-1FD9-496D-9943-99FB424DD214
ms.date: 12/05/2018
ms.keywords: ID3D12Tools, ID3D12Tools interface, ID3D12Tools interface,described, d3d12/ID3D12Tools, direct3d12.id3d12tools
f1_keywords:
- d3d12/ID3D12Tools
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D12.dll
api_name:
- ID3D12Tools
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D12Tools interface


## -description


This interface is used to configure the runtime for tools such as PIX. Its not intended or supported for any other scenario.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12Tools</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12Tools</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D12Tools</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12tools-enableshaderinstrumentation">EnableShaderInstrumentation</a>
</td>
<td align="left" width="63%">
This method enables tools such as PIX to instrument shaders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12tools-shaderinstrumentationenabled">ShaderInstrumentationEnabled</a>
</td>
<td align="left" width="63%">
Determines whether shader instrumentation is enabled.

</td>
</tr>
</table> 


## -remarks



Do not use this interface in your application, its not intended or supported for any scenario other than to enable tooling such as PIX.

Developer Mode must be enabled for this interface to respond.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d12/direct3d-12-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

