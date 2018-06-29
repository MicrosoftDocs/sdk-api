---
UID: NF:d3d11.ID3D11DeviceContext.ClearRenderTargetView
title: ID3D11DeviceContext::ClearRenderTargetView
author: windows-sdk-content
description: Set all the elements in a render target to one value.
old-location: direct3d11\id3d11devicecontext_clearrendertargetview.htm
old-project: direct3d11
ms.assetid: bbc6d3fb-b64f-47b0-9feb-a248dce0bf4b
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 2d296302-263e-a0b0-10ad-d1afbdf56ebf, ClearRenderTargetView, ClearRenderTargetView method [Direct3D 11], ClearRenderTargetView method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],ClearRenderTargetView method, ID3D11DeviceContext.ClearRenderTargetView, ID3D11DeviceContext::ClearRenderTargetView, d3d11/ID3D11DeviceContext::ClearRenderTargetView, direct3d11.id3d11devicecontext_clearrendertargetview
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11.h
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.ClearRenderTargetView
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::ClearRenderTargetView


## -description


Set all the elements in a render target to one value.


## -parameters




### -param pRenderTargetView [in]

Type: <b><a href="https://msdn.microsoft.com/3ae7c255-2403-493a-9fb9-fc9795f6d920">ID3D11RenderTargetView</a>*</b>

Pointer to the render target.


### -param ColorRGBA [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">FLOAT</a>[4]</b>

A 4-component array that represents the color to fill the render target with.


## -returns



Returns nothing.




## -remarks



Applications that wish to clear a render target to a specific integer value bit pattern should render a screen-aligned quad instead of using this method.  The reason for this is because this method accepts as input a floating point value, which may not have the same bit pattern as the original integer.

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 11/10:

Unlike Direct3D 9, the full extent of the resource view is always cleared. Viewport and scissor settings are not applied.

</td>
</tr>
</table>
 

When using <a href="https://msdn.microsoft.com/afbc1a02-1730-4502-af15-b668412d664c">D3D_FEATURE_LEVEL_9_x</a>, <a href="https://msdn.microsoft.com/library/Bb173539(v=VS.85).aspx">ClearRenderTargetView</a> only clears the first array slice in the render target view. This can impact (for example) cube map rendering scenarios. Applications should create a render target view for each face or array slice, then clear each view individually.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

