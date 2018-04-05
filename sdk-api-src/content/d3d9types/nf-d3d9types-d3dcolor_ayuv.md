---
UID: NF:d3d9types.D3DCOLOR_AYUV
title: D3DCOLOR_AYUV macro
author: windows-driver-content
description: Initializes a color using the (a,y,u,v) values.
old-location: direct3d9\d3dcolor_ayuv.htm
old-project: direct3d9
ms.assetid: VS|directx_sdk|~\d3dcolor_ayuv.htm
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: D3DCOLOR_AYUV, D3DCOLOR_AYUV macro [Direct3D 9], d3d9types/D3DCOLOR_AYUV, direct3d9.d3dcolor_ayuv, e980339c-1f00-2165-1680-e11cc0cedc4d
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
-	D3DCOLOR_AYUV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3DCOLOR_AYUV macro


## -description


Initializes a color using the (a,y,u,v) values.


## -parameters




### -param a

Alpha component of the color. This value must be in the range 0 through 255.


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



<a href="https://msdn.microsoft.com/e3091eaf-8639-428c-8dd8-6feeb7d7776e">D3DCOLOR_XYUV</a>



<a href="https://msdn.microsoft.com/cabb715a-2a6a-4d56-8113-5e5ed26fc107">Macros</a>
 

 

