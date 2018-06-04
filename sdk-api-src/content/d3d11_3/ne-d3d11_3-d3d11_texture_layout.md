---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3D11_TEXTURE_LAYOUT enumeration


## -description


Specifies texture layout options.


## -enum-fields




### -field D3D11_TEXTURE_LAYOUT_UNDEFINED

The texture layout is undefined, and is selected by the driver.


### -field D3D11_TEXTURE_LAYOUT_ROW_MAJOR

Data for the texture is stored in row major (sometimes called pitch-linear) order.


### -field D3D11_TEXTURE_LAYOUT_64K_STANDARD_SWIZZLE

A default texture uses the standardized swizzle pattern.


## -remarks



This enumeration controls the swizzle pattern of default textures and enable map support on default textures.  Callers must query <a href="https://msdn.microsoft.com/D0CD9245-D8BC-48E5-A69B-0DB9B87E56A4">D3D11_FEATURE_DATA_D3D11_OPTIONS2</a> to ensure that each option is supported.

The standard swizzle formats applies within each page-sized chunk, and pages are laid out in linear order with respect to one another.  A 16-bit interleave pattern defines the conversion from pre-swizzled intra-page location to the post-swizzled location.  

<img alt="Standard swizzle patterns" src="images/d3d11_standardswizzle.png"/>
To demonstrate, consider the 32bpp swizzle format above.  This is represented by the following interleave masks, where bits on the left are most-significant.

<pre class="syntax" xml:space="preserve"><code>UINT xBytesMask = 1010 1010 1000 1111
UINT yMask =      0101 0101 0111 0000
</code></pre>
To compute the swizzled address, the following code could be used (where the _pdep_u32 instruction is supported):

<pre class="syntax" xml:space="preserve"><code>UINT swizzledOffset = resourceBaseOffset +
                      _pdep_u32(xOffset, xBytesMask) + 
                      _pdep_u32(yOffset, yBytesMask);
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/b547819b-7006-40b5-84a4-adf198048051">Resource Enumerations</a>
 

 

