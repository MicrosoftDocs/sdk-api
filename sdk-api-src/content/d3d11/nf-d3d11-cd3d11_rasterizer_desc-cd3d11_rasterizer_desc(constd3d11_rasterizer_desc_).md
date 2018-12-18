---
UID: NF:d3d11.CD3D11_RASTERIZER_DESC.CD3D11_RASTERIZER_DESC(const D3D11_RASTERIZER_DESC &)
title: CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC(const D3D11_RASTERIZER_DESC &)
author: windows-sdk-content
description: Instantiates a new instance of a CD3D11_RASTERIZER_DESC structure that is initialized with default rasterizer-state values.
old-location: direct3d11\cd3d11_rasterizer_desc_cd3d11_rasterizer_desc_cd3d11_default_.htm
tech.root: direct3d11
ms.assetid: 6D2B2D68-C3ED-460F-B253-583A1DEF5DAA
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CD3D11_RASTERIZER_DESC, CD3D11_RASTERIZER_DESC constructor [Direct3D 11], CD3D11_RASTERIZER_DESC constructor [Direct3D 11],CD3D11_RASTERIZER_DESC interface, CD3D11_RASTERIZER_DESC interface [Direct3D 11],CD3D11_RASTERIZER_DESC constructor, CD3D11_RASTERIZER_DESC.CD3D11_RASTERIZER_DESC, CD3D11_RASTERIZER_DESC.CD3D11_RASTERIZER_DESC(const D3D11_RASTERIZER_DESC &), CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC, CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC(CD3D11_DEFAULT), CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC(const D3D11_RASTERIZER_DESC &), d3d11/CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC, direct3d11.cd3d11_rasterizer_desc_cd3d11_rasterizer_desc_cd3d11_default_
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - CD3D11_RASTERIZER_DESC.CD3D11_RASTERIZER_DESC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CD3D11_RASTERIZER_DESC::CD3D11_RASTERIZER_DESC(const D3D11_RASTERIZER_DESC &)


## -description


Instantiates a new instance of a <a href="https://msdn.microsoft.com/3A64A02B-9DF6-46D1-8695-9B92F25CE620">CD3D11_RASTERIZER_DESC</a> structure that is initialized with default rasterizer-state values.


## -parameters




### -param o

TBD






## -remarks



Here are the default rasterizer-state values for the members of <a href="https://msdn.microsoft.com/53252fef-f557-46d1-b6a7-ccc8a059752a">D3D11_RASTERIZER_DESC</a>:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>FillMode = D3D11_FILL_SOLID;
        CullMode = D3D11_CULL_BACK;
        FrontCounterClockwise = FALSE;
        DepthBias = D3D11_DEFAULT_DEPTH_BIAS;
        DepthBiasClamp = D3D11_DEFAULT_DEPTH_BIAS_CLAMP;
        SlopeScaledDepthBias = D3D11_DEFAULT_SLOPE_SCALED_DEPTH_BIAS;
        DepthClipEnable = TRUE;
        ScissorEnable = FALSE;
        MultisampleEnable = FALSE;
        AntialiasedLineEnable = FALSE;
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3A64A02B-9DF6-46D1-8695-9B92F25CE620">CD3D11_RASTERIZER_DESC</a>
 

 

