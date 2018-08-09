---
UID: NS:dxgitype._D3DCOLORVALUE
title: "_D3DCOLORVALUE"
author: windows-sdk-content
description: Represents a color value with alpha, which is used for transparency.
old-location: direct3ddxgi\d3dcolorvalue.htm
old-project: direct3ddxgi
ms.assetid: 27A86A10-FC0E-421E-BEA7-2DEB539849BB
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: D3DCOLORVALUE, D3DCOLORVALUE structure [DXGI], DXGI_RGBA, _D3DCOLORVALUE, direct3ddxgi.d3dcolorvalue, dxgitype/D3DCOLORVALUE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxgitype.h
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
tech.root: 
req.typenames: D3DCOLORVALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgitype.h
api_name:
 - D3DCOLORVALUE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _D3DCOLORVALUE structure


## -description


Represents a color value with alpha, which is used for transparency.
        


## -struct-fields




### -field r

Floating-point value that specifies the red component of a color. This value generally is in the range from 0.0 through 1.0. A value of 0.0 indicates the complete absence of the red component, while a value of 1.0 indicates that red is fully present.
          


### -field g

Floating-point value that specifies the green component of a color. This value generally is in the range from 0.0 through 1.0. A value of 0.0 indicates the complete absence of the green component, while a value of 1.0 indicates that green is fully present.
          


### -field b

Floating-point value that specifies the blue component of a color. This value generally is in the range from 0.0 through 1.0. A value of 0.0 indicates the complete absence of the blue component, while a value of 1.0 indicates that blue is fully present.
          


### -field a

Floating-point value that specifies the alpha component of a color. This value generally is in the range from 0.0 through 1.0. A value of 0.0 indicates fully transparent, while a value of 1.0 indicates fully opaque.
          


## -remarks



You can set the members of this structure to values outside the range of 0 through 1 to implement some unusual effects.
          Values greater than 1 produce strong lights that tend to wash out a scene.
          Negative values produce dark lights that actually remove light from a scene.
        

The DXGItype.h header type-defines <a href="https://msdn.microsoft.com/5F9DDDC1-644E-4DA2-8E3D-F157789809E7">DXGI_RGBA</a> as an alias of <b>D3DCOLORVALUE</b>, as follows:
        

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>typedef D3DCOLORVALUE DXGI_RGBA;</pre>
</td>
</tr>
</table></span></div>
You can use D3DCOLORVALUE or <a href="https://msdn.microsoft.com/5F9DDDC1-644E-4DA2-8E3D-F157789809E7">DXGI_RGBA</a> with <a href="https://msdn.microsoft.com/E46CA219-303F-40D4-8C62-6241C9199BA0">IDXGISwapChain1::SetBackgroundColor</a>, <a href="https://msdn.microsoft.com/AF10BAF1-5C49-45E7-B776-3EB606C02E10">IDXGISwapChain1::GetBackgroundColor</a>, and <a href="https://msdn.microsoft.com/DD3D1E49-06D2-4FB9-A41B-86453D8E566F">DXGI_ALPHA_MODE</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>



<a href="https://msdn.microsoft.com/5F9DDDC1-644E-4DA2-8E3D-F157789809E7">DXGI_RGBA</a>
 

 

