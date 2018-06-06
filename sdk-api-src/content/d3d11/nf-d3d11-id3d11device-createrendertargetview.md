---
UID: NF:d3d11.ID3D11Device.CreateRenderTargetView
title: ID3D11Device::CreateRenderTargetView
author: windows-sdk-content
description: Creates a render-target view for accessing resource data.
old-location: direct3d11\id3d11device_createrendertargetview.htm
old-project: direct3d11
ms.assetid: e757c959-f0ac-44c3-8226-b9f0b1c2a031
ms.author: windowssdkdev
ms.date: 04/06/2018
ms.keywords: 02715db5-c01a-06db-fe93-51594d87921b, CreateRenderTargetView, CreateRenderTargetView method [Direct3D 11], CreateRenderTargetView method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CreateRenderTargetView method, ID3D11Device.CreateRenderTargetView, ID3D11Device::CreateRenderTargetView, d3d11/ID3D11Device::CreateRenderTargetView, direct3d11.id3d11device_createrendertargetview
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
 - ID3D11Device.CreateRenderTargetView
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device::CreateRenderTargetView


## -description


Creates a render-target view for accessing resource data.


## -parameters




### -param pResource [in]

Type: <b><a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/3823ec00-cb3c-43ce-9f1a-be4e1e99d587">ID3D11Resource</a> that represents a render target. This resource must have been created with the <a href="https://msdn.microsoft.com/4ffa1714-bd85-4d5a-930d-20526f46e4b9">D3D11_BIND_RENDER_TARGET</a> flag.


### -param pDesc [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/b154ac98-49ed-4d00-8cb6-5e57680e125c">D3D11_RENDER_TARGET_VIEW_DESC</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/b154ac98-49ed-4d00-8cb6-5e57680e125c">D3D11_RENDER_TARGET_VIEW_DESC</a> that represents a render-target view description. Set this parameter to <b>NULL</b> to create a view that accesses all of the subresources in mipmap level 0.


### -param ppRTView [out, optional]

Type: <b><a href="https://msdn.microsoft.com/3ae7c255-2403-493a-9fb9-fc9795f6d920">ID3D11RenderTargetView</a>**</b>

Address of a pointer to an <a href="https://msdn.microsoft.com/3ae7c255-2403-493a-9fb9-fc9795f6d920">ID3D11RenderTargetView</a>. Set this parameter to <b>NULL</b> to validate the other input parameters (the method will return S_FALSE if the other input parameters pass validation).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



A render-target view can be bound to the output-merger stage by calling <a href="https://msdn.microsoft.com/65514812-7433-4c13-a6cb-53980dacdf65">ID3D11DeviceContext::OMSetRenderTargets</a>.

The Direct3D 11.1 runtime, which is available starting with Windows 8, allows you to use <b>CreateRenderTargetView</b> for the following new purpose. 

You can create render-target views of video resources so that Direct3D shaders can process those render-target views. These video resources are either <a href="https://msdn.microsoft.com/e4f9cfd8-65e6-4375-8f87-736bca32cad4">Texture2D</a> or <a href="https://msdn.microsoft.com/78ab2feb-4d67-4f6f-bffe-48d55183ce28">Texture2DArray</a>. The value in the <b>ViewDimension</b> member of the <a href="https://msdn.microsoft.com/b154ac98-49ed-4d00-8cb6-5e57680e125c">D3D11_RENDER_TARGET_VIEW_DESC</a> structure for a created render-target view must match the type of video resource, D3D11_RTV_DIMENSION_TEXTURE2D          for Texture2D and D3D11_RTV_DIMENSION_TEXTURE2DARRAY for Texture2DArray. Additionally, the format of the underlying video resource restricts the formats that the view can use. The video resource format values on the <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a> reference page specify the format values that views are restricted to.

The runtime read+write conflict prevention logic (which stops a resource from being bound as an SRV and RTV or UAV at the same time) treats views of different parts of the same video surface as conflicting for simplicity.  Therefore, the runtime does not allow an application to read from luma while the application simultaneously renders to chroma in the same surface even though the hardware might allow these simultaneous operations.




## -see-also




<a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a>
 

 

