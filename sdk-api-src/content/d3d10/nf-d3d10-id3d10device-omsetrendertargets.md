---
UID: NF:d3d10.ID3D10Device.OMSetRenderTargets
title: ID3D10Device::OMSetRenderTargets
author: windows-sdk-content
description: Bind one or more render targets and the depth-stencil buffer to the output-merger stage.
old-location: direct3d10\id3d10device_omsetrendertargets.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_omsetrendertargets.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 1a066759-273f-afca-4fed-6d836735ff9f, ID3D10Device interface [Direct3D 10],OMSetRenderTargets method, ID3D10Device.OMSetRenderTargets, ID3D10Device::OMSetRenderTargets, OMSetRenderTargets, OMSetRenderTargets method [Direct3D 10], OMSetRenderTargets method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::OMSetRenderTargets, direct3d10.id3d10device_omsetrendertargets
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d10.h
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
req.typenames: D3D10_USAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.OMSetRenderTargets
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Device::OMSetRenderTargets


## -description


Bind one or more render targets and the depth-stencil buffer to the <a href="https://msdn.microsoft.com/8be68c15-2deb-4804-b683-30080a876189">output-merger stage</a>.


## -parameters




### -param NumViews [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of render targets to bind.


### -param ppRenderTargetViews [in]

Type: <b><a href="https://msdn.microsoft.com/0a545476-19d2-41f7-9012-82fbf633f23b">ID3D10RenderTargetView</a>*</b>

Pointer to an array of render targets (see <a href="https://msdn.microsoft.com/0a545476-19d2-41f7-9012-82fbf633f23b">ID3D10RenderTargetView</a>) to bind to the device. If this parameter is <b>NULL</b>, no render targets are bound. See Remarks.


### -param pDepthStencilView [in]

Type: <b><a href="https://msdn.microsoft.com/b88f3b61-4549-4ef7-9dda-0c2ed247d2f1">ID3D10DepthStencilView</a>*</b>

Pointer to a depth-stencil view (see <a href="https://msdn.microsoft.com/b88f3b61-4549-4ef7-9dda-0c2ed247d2f1">ID3D10DepthStencilView</a>) to bind to the device. If this parameter is <b>NULL</b>, the depth-stencil state is not bound.


## -returns



Returns nothing.




## -remarks



A call to <b>OMSetRenderTargets</b> overrides all bounded render targets and the depth stencil target regardless of the number of render targets in <i>ppRenderTargetViews</i>.

The maximum number of render targets a device can have active at any given time is set by a #define in D3D10.h called D3D10_SIMULTANEOUS_RENDER_TARGET_COUNT. It is invalid to try to set the same <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">subresource</a> to multiple render target slots.

If any subresources are also currently bound for reading or writing (perhaps in a different part of the <a href="https://msdn.microsoft.com/3ead6c7c-c7cc-48f1-81d5-b4b67326d610">pipeline</a>), those bind points will be <b>NULL</b>'ed out to prevent the same subresource from being read and written simultaneously in a single rendering operation.

The method will not hold references to the interfaces passed in. For that reason, applications should be careful not to release interfaces currently in use by the device.

See <a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">Binding Resources and Pipeline stages</a> for more information on binding resources.

The pixel shader must be able to simultaneously render to at least eight separate render targets. All of these render targets must access the same type of resource: <a href="https://msdn.microsoft.com/7f552b9b-c5fb-4bc2-a7ae-61983379db38">Buffer</a>, <a href="https://msdn.microsoft.com/5f6fd0e4-a73e-4d13-b3a0-c884b7912581">Texture1D</a>, <a href="https://msdn.microsoft.com/3d793423-3d79-48c1-aa78-f9d93b79e0b6">Texture1DArray</a>, <a href="https://msdn.microsoft.com/e4f9cfd8-65e6-4375-8f87-736bca32cad4">Texture2D</a>, <a href="https://msdn.microsoft.com/78ab2feb-4d67-4f6f-bffe-48d55183ce28">Texture2DArray</a>, <a href="https://msdn.microsoft.com/a3640aac-b503-4716-8bc6-105e96bea03c">Texture3D</a>, or <a href="https://msdn.microsoft.com/e8cb483a-d831-4942-b6fe-61dd5edb1813">TextureCube</a>. All render targets must have the same size in all dimensions (width and height, and depth for 3D or array size for *Array types). If render targets use multisample anti-aliasing, all bound render targets and depth buffer must be the same form of multisample resource (that is, the sample counts must be the same). Each render target can have a different data format. These render target formats are not required to have identical bit-per-element counts.

Any combination of the eight slots for render targets can have a render target set or not set.

The same resource view cannot be bound to multiple render target slots simultaneously. However, you can set multiple non-overlapping resource views of a single resource as simultaneous multiple render targets.




## -see-also




<a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a>
 

 

