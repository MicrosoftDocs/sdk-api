---
UID: NF:d3d11.ID3D11DeviceContext.OMGetRenderTargetsAndUnorderedAccessViews
title: ID3D11DeviceContext::OMGetRenderTargetsAndUnorderedAccessViews
author: windows-sdk-content
description: Get pointers to the resources bound to the output-merger stage.
old-location: direct3d11\id3d11devicecontext_omgetrendertargetsandunorderedaccessviews.htm
tech.root: direct3d11
ms.assetid: 5baaedea-5db4-4a25-adfc-2ac9cf48ad6d
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: 84c4c039-405e-ee3a-22d0-80eb7078ffe8, ID3D11DeviceContext interface [Direct3D 11],OMGetRenderTargetsAndUnorderedAccessViews method, ID3D11DeviceContext.OMGetRenderTargetsAndUnorderedAccessViews, ID3D11DeviceContext::OMGetRenderTargetsAndUnorderedAccessViews, OMGetRenderTargetsAndUnorderedAccessViews, OMGetRenderTargetsAndUnorderedAccessViews method [Direct3D 11], OMGetRenderTargetsAndUnorderedAccessViews method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::OMGetRenderTargetsAndUnorderedAccessViews, direct3d11.id3d11devicecontext_omgetrendertargetsandunorderedaccessviews
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11DeviceContext.OMGetRenderTargetsAndUnorderedAccessViews
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::OMGetRenderTargetsAndUnorderedAccessViews


## -description


Get pointers to the resources bound to the output-merger stage.


## -parameters




### -param NumRTVs [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The number of render-target views to retrieve.


### -param ppRenderTargetViews [out, optional]

Type: <b><a href="https://msdn.microsoft.com/3ae7c255-2403-493a-9fb9-fc9795f6d920">ID3D11RenderTargetView</a>**</b>

Pointer to an array of <a href="https://msdn.microsoft.com/3ae7c255-2403-493a-9fb9-fc9795f6d920">ID3D11RenderTargetView</a>s, which represent render-target views. Specify <b>NULL</b> for this parameter when retrieval of render-target views is not required.
          


### -param ppDepthStencilView [out, optional]

Type: <b><a href="https://msdn.microsoft.com/10be1fd1-8700-4c0a-b447-d3c2569f8e81">ID3D11DepthStencilView</a>**</b>

Pointer to a <a href="https://msdn.microsoft.com/10be1fd1-8700-4c0a-b447-d3c2569f8e81">ID3D11DepthStencilView</a>, which represents a depth-stencil view. Specify <b>NULL</b> for this parameter when retrieval of the depth-stencil view is not required.
          


### -param UAVStartSlot [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Index into a zero-based array to begin retrieving unordered-access views (ranges from 0 to D3D11_PS_CS_UAV_REGISTER_COUNT - 1).
            For pixel shaders <i>UAVStartSlot</i> should be equal to the number of render-target views that are bound.
          


### -param NumUAVs [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of unordered-access views to return in <i>ppUnorderedAccessViews</i>. This number ranges from 0 to D3D11_PS_CS_UAV_REGISTER_COUNT - <i>UAVStartSlot</i>.
          


### -param ppUnorderedAccessViews [out, optional]

Type: <b><a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>**</b>

Pointer to an array of <a href="https://msdn.microsoft.com/9def4a7d-f145-4073-8d7d-bf3c7ac7a060">ID3D11UnorderedAccessView</a>s, which represent unordered-access views that are retrieved. Specify <b>NULL</b> for this parameter when retrieval of unordered-access views is not required.
          


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> on the returned interfaces when they are no longer needed to avoid memory leaks.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

