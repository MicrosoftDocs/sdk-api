---
UID: NF:d3d9.IDirect3DDevice9Ex.SetConvolutionMonoKernel
title: IDirect3DDevice9Ex::SetConvolutionMonoKernel
author: windows-sdk-content
description: Prepare the texture sampler for monochrome convolution filtering on a single-color texture.
old-location: direct3d9\idirect3ddevice9ex_setconvolutionmonokernel.htm
tech.root: direct3d9
ms.assetid: VS|directx_sdk|~\idirect3ddevice9ex_setconvolutionmonokernel.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 901624bb-e4a4-a7b5-0f2f-bf89649a1105, IDirect3DDevice9Ex interface [Direct3D 9],SetConvolutionMonoKernel method, IDirect3DDevice9Ex.SetConvolutionMonoKernel, IDirect3DDevice9Ex::SetConvolutionMonoKernel, SetConvolutionMonoKernel, SetConvolutionMonoKernel method [Direct3D 9], SetConvolutionMonoKernel method [Direct3D 9],IDirect3DDevice9Ex interface, d3d9/IDirect3DDevice9Ex::SetConvolutionMonoKernel, direct3d9.idirect3ddevice9ex_setconvolutionmonokernel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d9.h
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
req.lib: D3D9.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D9.lib
 - D3D9.dll
api_name:
 - IDirect3DDevice9Ex.SetConvolutionMonoKernel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d9.h
: 
- IDirect3DDevice9Ex.SetConvolutionMonoKernel
: 
---

# IDirect3DDevice9Ex::SetConvolutionMonoKernel


## -description


Prepare the texture sampler for monochrome convolution filtering on a single-color texture.


## -parameters




### -param width [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The width of the filter kernel; ranging from 1 - <a href="https://msdn.microsoft.com/en-us/library/Bb509548(v=VS.85).aspx">D3DCONVOLUTIONMONO_MAXWIDTH</a>. The default value is 1.


### -param height [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The height of the filter kernel; ranging from 1 - <a href="https://msdn.microsoft.com/en-us/library/Bb509548(v=VS.85).aspx">D3DCONVOLUTIONMONO_MAXHEIGHT</a>. The default value is 1.


### -param rows [in]

Type: <b>float*</b>

An array of weights, one weight for each kernel sub-element in the width. This parameter must be <b>NULL</b>, which will set the weights equal to the default value.


### -param columns [in]

Type: <b>float*</b>

An array of weights, one weight for each kernel sub-element in the height. This parameter must be <b>NULL</b>, which will set the weights equal to the default value.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK.




## -remarks



This method is designed to filter a single color texture. A monochrome convolution filter is a 2D box filter with all of the weights set to 1.0;  the filter kernel resolution ranges from 1 x 1 to 7 x 7. When monochrome texture filtering is set to a texture sampler and texture sampling is performed at location, then Direct3D performs convolution. 

Restrictions include:

<ul>
<li>The filter specified by this method is recorded in state blocks as a part of <a href="https://msdn.microsoft.com/en-us/library/Bb172608(v=VS.85).aspx">D3DSBT_PIXELSTATE</a>.</li>
<li>The only texture address mode supported is: <a href="https://msdn.microsoft.com/en-us/library/Bb172593(v=VS.85).aspx">D3DPTADDRESSCAPS_BORDER</a>; the border color is always 0.</li>
<li>This method is not supported for mipmaps.</li>
<li>Using a non-monochrome texture with convolution filtering will generate a driver error.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174337(v=VS.85).aspx">IDirect3DDevice9Ex</a>
 

 

