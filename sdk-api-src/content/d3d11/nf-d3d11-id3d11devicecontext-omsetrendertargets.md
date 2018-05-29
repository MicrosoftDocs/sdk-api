---
UID: NF:d3d11.ID3D11DeviceContext.OMSetRenderTargets
title: ID3D11DeviceContext::OMSetRenderTargets
author: windows-sdk-content
description: Bind one or more render targets atomically and the depth-stencil buffer to the output-merger stage.
old-location: direct3d11\id3d11devicecontext_omsetrendertargets.htm
old-project: direct3d11
ms.assetid: 65514812-7433-4c13-a6cb-53980dacdf65
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 57e16a81-6543-5ac7-d96c-aac3ca8504f8, ID3D11DeviceContext interface [Direct3D 11],OMSetRenderTargets method, ID3D11DeviceContext.OMSetRenderTargets, ID3D11DeviceContext::OMSetRenderTargets, OMSetRenderTargets, OMSetRenderTargets method [Direct3D 11], OMSetRenderTargets method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::OMSetRenderTargets, direct3d11.id3d11devicecontext_omsetrendertargets
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11DeviceContext.OMSetRenderTargets
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::OMSetRenderTargets


## -description


Bind one or more render targets atomically and the depth-stencil buffer to the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger stage</a>.


## -parameters




### -param NumViews [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of render targets to bind (ranges between 0 and <b>D3D11_SIMULTANEOUS_RENDER_TARGET_COUNT</b>). If this parameter is nonzero, the number of entries in the array to which <i>ppRenderTargetViews</i> points must equal the number in this parameter.


### -param ppRenderTargetViews [in, optional]

Type: <b><a href="https://msdn.microsoft.com/3ae7c255-2403-493a-9fb9-fc9795f6d920">ID3D11RenderTargetView</a>*</b>

Pointer to an array of <a href="https://msdn.microsoft.com/3ae7c255-2403-493a-9fb9-fc9795f6d920">ID3D11RenderTargetView</a> that represent the render targets to bind to the device. 
        If this parameter is <b>NULL</b> and <i>NumViews</i> is 0, no render targets are bound.


### -param pDepthStencilView [in, optional]

Type: <b><a href="https://msdn.microsoft.com/10be1fd1-8700-4c0a-b447-d3c2569f8e81">ID3D11DepthStencilView</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/10be1fd1-8700-4c0a-b447-d3c2569f8e81">ID3D11DepthStencilView</a> that represents the depth-stencil view to bind to the device. 
        If this parameter is <b>NULL</b>, the depth-stencil state is not bound.


## -returns



Returns nothing.




## -remarks



The maximum number of active render targets a device can have active at any given time is set by a #define in D3D11.h called 
      <b>D3D11_SIMULTANEOUS_RENDER_TARGET_COUNT</b>. It is invalid to try to set the same subresource to multiple render target slots. 
      Any render targets not defined by this call are set to <b>NULL</b>.

If any subresources are also currently bound for reading in a different stage or writing (perhaps in a different part of the pipeline), 
      those bind points will be set to <b>NULL</b>, in order to prevent the same subresource from being read and written simultaneously in a single rendering operation.


        The method will hold a reference to the interfaces passed in.
        This differs from the device state behavior in Direct3D 10.
      

If the render-target views were created from an array resource type, all of the render-target views must have the same array size.  
      This restriction also applies to the depth-stencil view, its array size must match that of the render-target views being bound.

The pixel shader must be able to simultaneously render to at least eight separate render targets. All of these render targets must access the same type of resource: <a href="https://msdn.microsoft.com/7f552b9b-c5fb-4bc2-a7ae-61983379db38">Buffer</a>, <a href="https://msdn.microsoft.com/5f6fd0e4-a73e-4d13-b3a0-c884b7912581">Texture1D</a>, <a href="https://msdn.microsoft.com/3d793423-3d79-48c1-aa78-f9d93b79e0b6">Texture1DArray</a>, <a href="https://msdn.microsoft.com/e4f9cfd8-65e6-4375-8f87-736bca32cad4">Texture2D</a>, <a href="https://msdn.microsoft.com/78ab2feb-4d67-4f6f-bffe-48d55183ce28">Texture2DArray</a>, <a href="https://msdn.microsoft.com/a3640aac-b503-4716-8bc6-105e96bea03c">Texture3D</a>, or <a href="https://msdn.microsoft.com/e8cb483a-d831-4942-b6fe-61dd5edb1813">TextureCube</a>. All render targets must have the same size in all dimensions (width and height, and depth for 3D or array size for *Array types). If render targets use multisample anti-aliasing, all bound render targets and depth buffer must be the same form of multisample resource (that is, the sample counts must be the same). Each render target can have a different data format. These render target formats are not required to have identical bit-per-element counts.

Any combination of the eight slots for render targets can have a render target set or not set.

The same resource view cannot be bound to multiple render target slots simultaneously. However, you can set multiple non-overlapping resource views of a single resource as simultaneous multiple render targets.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

