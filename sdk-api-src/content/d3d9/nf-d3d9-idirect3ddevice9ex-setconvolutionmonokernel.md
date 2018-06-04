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

# IDirect3DDevice9Ex::SetConvolutionMonoKernel


## -description


Prepare the texture sampler for monochrome convolution filtering on a single-color texture.


## -parameters




### -param width




### -param height




### -param rows




### -param columns






#### - ColumnWeights [in]

Type: <b>float*</b>

An array of weights, one weight for each kernel sub-element in the height. This parameter must be <b>NULL</b>, which will set the weights equal to the default value.


#### - Height [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The height of the filter kernel; ranging from 1 - <a href="https://msdn.microsoft.com/bc7c36fd-b905-47e7-a38f-1139a8337121">D3DCONVOLUTIONMONO_MAXHEIGHT</a>. The default value is 1.


#### - RowWeights [in]

Type: <b>float*</b>

An array of weights, one weight for each kernel sub-element in the width. This parameter must be <b>NULL</b>, which will set the weights equal to the default value.


#### - Width [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The width of the filter kernel; ranging from 1 - <a href="https://msdn.microsoft.com/bc7c36fd-b905-47e7-a38f-1139a8337121">D3DCONVOLUTIONMONO_MAXWIDTH</a>. The default value is 1.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.




## -remarks



This method is designed to filter a single color texture. A monochrome convolution filter is a 2D box filter with all of the weights set to 1.0;  the filter kernel resolution ranges from 1 x 1 to 7 x 7. When monochrome texture filtering is set to a texture sampler and texture sampling is performed at location, then Direct3D performs convolution. 

Restrictions include:

<ul>
<li>The filter specified by this method is recorded in state blocks as a part of <a href="https://msdn.microsoft.com/60b94d45-aab6-4dbe-ab48-65dfe9861d82">D3DSBT_PIXELSTATE</a>.</li>
<li>The only texture address mode supported is: <a href="https://msdn.microsoft.com/4434e456-670e-46a9-ba78-affdc195fe1c">D3DPTADDRESSCAPS_BORDER</a>; the border color is always 0.</li>
<li>This method is not supported for mipmaps.</li>
<li>Using a non-monochrome texture with convolution filtering will generate a driver error.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b2132ee3-5888-4cfe-a7c7-1134c0418a37">IDirect3DDevice9Ex</a>
 

 

