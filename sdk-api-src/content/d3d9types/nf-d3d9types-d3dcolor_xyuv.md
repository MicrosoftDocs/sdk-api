---
UID: NF:d3d9types.D3DCOLOR_XYUV
title: D3DCOLOR_XYUV macro
author: windows-driver-content
description: Initializes a color with the (y, u, v) values.
old-location: direct3d9\d3dcolor_xyuv.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dcolor_xyuv.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DCOLOR_XYUV, D3DCOLOR_XYUV macro [Direct3D 9], d3d9types/D3DCOLOR_XYUV, direct3d9.d3dcolor_xyuv, fae0d556-f689-743e-81ee-07cb785bece0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: d3d9types.h
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
req.typenames: D3DZBUFFERTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	D3d9types.h
api_name:
-	D3DCOLOR_XYUV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3DCOLOR_XYUV macro


## -description


Initializes a color with the (y, u, v) values.


## -parameters




### -param y

Luminance component of the color. This value must be in the range 0 through 255.


### -param u

Blue brightness of the color. This value must be in the range 0 through 255.


### -param v

Red brightness of the color. This value must be in the range 0 through 255.


## -remarks



An RGB color can be reduced to 16 bits per pixel by conversion to luminance and color differences with the following equations:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
y (luminance) = 0.299*red + 0.587*green + 0.114*blue
u = blue - luminance
v = red - luminance 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e862ba1b-fdcf-4058-8835-e58b4fc5e21a">D3DCOLOR_ARGB</a>



<a href="https://msdn.microsoft.com/47b65aab-511a-44c1-ab94-973bc2da7e04">D3DCOLOR_AYUV</a>



<a href="https://msdn.microsoft.com/cabb715a-2a6a-4d56-8113-5e5ed26fc107">Macros</a>
 

 

