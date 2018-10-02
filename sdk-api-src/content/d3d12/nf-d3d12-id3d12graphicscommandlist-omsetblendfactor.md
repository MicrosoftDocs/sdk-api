---
UID: NF:d3d12.ID3D12GraphicsCommandList.OMSetBlendFactor
title: ID3D12GraphicsCommandList::OMSetBlendFactor
author: windows-sdk-content
description: Sets the blend factor that modulate values for a pixel shader, render target, or both.
old-location: direct3d12\id3d12graphicscommandlist_omsetblendfactor.htm
tech.root: direct3d12
ms.assetid: 344FD8B5-7225-4BEC-9D1F-C9CEDFE8C60F
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ID3D12GraphicsCommandList interface,OMSetBlendFactor method, ID3D12GraphicsCommandList.OMSetBlendFactor, ID3D12GraphicsCommandList::OMSetBlendFactor, OMSetBlendFactor, OMSetBlendFactor method, OMSetBlendFactor method,ID3D12GraphicsCommandList interface, d3d12/ID3D12GraphicsCommandList::OMSetBlendFactor, direct3d12.id3d12graphicscommandlist_omsetblendfactor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12GraphicsCommandList.OMSetBlendFactor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList::OMSetBlendFactor


## -description


Sets the blend factor that modulate values for a pixel shader, render target, or both.


## -parameters




### -param BlendFactor [in, optional]

Type: <b>const FLOAT[4]</b>

Array of blend factors, one for each RGBA component.
          


## -returns



This method does not return a value.
          




## -remarks



If you created the blend-state object with D3D11_BLEND_BLEND_FACTOR or D3D11_BLEND_INV_BLEND_FACTOR, the blending stage uses the non-NULL array of blend factors.
      

If you didn't create the blend-state object with D3D11_BLEND_BLEND_FACTOR or D3D11_BLEND_INV_BLEND_FACTOR, the blending stage does not use the non-NULL array of blend factors; the runtime stores the blend factors.
      

If you pass NULL, the runtime uses or stores a blend factor equal to { 1, 1, 1, 1 }.
      

D3D11_BLEND_BLEND_FACTOR and D3D11_BLEND_INV_BLEND_FACTOR are <a href="https://msdn.microsoft.com/en-us/library/Dn770338(v=VS.85).aspx">D3D12_BLEND</a> enumeration constants.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn903537(v=VS.85).aspx">ID3D12GraphicsCommandList</a>
 

 

