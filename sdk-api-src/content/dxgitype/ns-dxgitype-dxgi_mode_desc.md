---
UID: NS:dxgitype.DXGI_MODE_DESC
title: DXGI_MODE_DESC
author: windows-sdk-content
description: Describes a display mode.
old-location: direct3ddxgi\dxgi_mode_desc.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_mode_desc.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: 1aeacbf7-89bc-3882-6962-2a7219bdc055, DXGI_MODE_DESC, DXGI_MODE_DESC structure [DXGI], direct3ddxgi.dxgi_mode_desc, dxgitype/DXGI_MODE_DESC
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
req.typenames: DXGI_MODE_DESC
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgitype.h
api_name:
 - DXGI_MODE_DESC
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_MODE_DESC structure


## -description


Describes a display mode.


## -struct-fields




### -field Width

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value that describes the resolution width. If you specify the width as zero when you call the  <a href="https://msdn.microsoft.com/c6c32336-fbea-420b-b0d9-1c1cf3893688">IDXGIFactory::CreateSwapChain</a> method to create a swap chain, the runtime obtains the width from the output window and assigns this width value to the swap-chain description. You can subsequently call the <a href="https://msdn.microsoft.com/8265f4bf-1d4f-4117-9316-a399e028af60">IDXGISwapChain::GetDesc</a> method to retrieve the assigned width value.


### -field Height

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value describing the resolution height. If you specify the height as zero when you call the  <a href="https://msdn.microsoft.com/c6c32336-fbea-420b-b0d9-1c1cf3893688">IDXGIFactory::CreateSwapChain</a> method to create a swap chain, the runtime obtains the height from the output window and assigns this height value to the swap-chain description. You can subsequently call the <a href="https://msdn.microsoft.com/8265f4bf-1d4f-4117-9316-a399e028af60">IDXGISwapChain::GetDesc</a> method to retrieve the assigned height value.


### -field RefreshRate

Type: <b><a href="https://msdn.microsoft.com/0a878d11-dc90-4cad-bde5-54a135e53a86">DXGI_RATIONAL</a></b>

A <a href="https://msdn.microsoft.com/0a878d11-dc90-4cad-bde5-54a135e53a86">DXGI_RATIONAL</a> structure describing the refresh rate in hertz


### -field Format

Type: <b><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a></b>

A <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> structure describing the display format.


### -field ScanlineOrdering

Type: <b><a href="https://msdn.microsoft.com/ecb66eed-9368-4cac-82e9-0e32c41e3ec5">DXGI_MODE_SCANLINE_ORDER</a></b>

A member of the <a href="https://msdn.microsoft.com/ecb66eed-9368-4cac-82e9-0e32c41e3ec5">DXGI_MODE_SCANLINE_ORDER</a> enumerated type describing the scanline drawing mode.


### -field Scaling

Type: <b><a href="https://msdn.microsoft.com/2f9c16c6-b2d2-4135-8399-fd37aece3286">DXGI_MODE_SCALING</a></b>

A member of the <a href="https://msdn.microsoft.com/2f9c16c6-b2d2-4135-8399-fd37aece3286">DXGI_MODE_SCALING</a> enumerated type describing the scaling mode.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/3d791b9b-f9e8-443c-ac7a-fc4faa3eaf95">GetDisplayModeList</a> and <a href="https://msdn.microsoft.com/f531ee0d-d934-4ab2-bb7a-2c29f521f4cb">FindClosestMatchingMode</a> methods.

The following format values are valid for display modes and when you create a bit-block transfer (bitblt) model swap chain. The valid values depend on the feature level that you are working with.

<ul>
<li>
Feature level &gt;= 9.1

<ul>
<li>
<a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_R8G8B8A8_UNORM</a>
</li>
<li><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</a></li>
<li>
<a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_B8G8R8A8_UNORM</a> (except 10.x on Windows Vista)</li>
<li><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</a> (except 10.x on Windows Vista)</li>
</ul>
</li>
<li>
Feature level &gt;= 10.0

<ul>
<li>
<a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_R16G16B16A16_FLOAT</a>
</li>
<li><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_R10G10B10A2_UNORM</a></li>
</ul>
</li>
<li>
Feature level &gt;= 11.0

<ul>
<li><a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM</a></li>
</ul>
</li>
</ul>
You can pass one of these format values to <a href="https://msdn.microsoft.com/d5442fe8-e510-4bda-9df0-377b465cdd5e">ID3D11Device::CheckFormatSupport</a> to determine if it is a valid format for displaying on screen. If <b>ID3D11Device::CheckFormatSupport</b> returns <b>D3D11_FORMAT_SUPPORT_DISPLAY</b> in the bit field to which the <i>pFormatSupport</i> parameter points, the format is valid for displaying on screen.

Starting with Windows 8 for a flip model swap chain (that is, a swap chain that has the <a href="DXGI_SWAP_EFFECT.htm">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> value set in the <b>SwapEffect</b> member of <a href="https://msdn.microsoft.com/819d4ff3-f717-46ab-a626-cff065681c79">DXGI_SWAP_CHAIN_DESC</a>), you must set the <b>Format</b> member of <b>DXGI_MODE_DESC</b> to <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_R16G16B16A16_FLOAT</a>, <b>DXGI_FORMAT_B8G8R8A8_UNORM</b>, or <b>DXGI_FORMAT_R8G8B8A8_UNORM</b>.

Because of the relaxed render target creation rules that Direct3D 11 has for back buffers, applications can create a <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT_B8G8R8A8_UNORM_SRGB</a> render target view from a <b>DXGI_FORMAT_B8G8R8A8_UNORM</b> swap chain so they can use automatic color space conversion when they render the swap chain.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

