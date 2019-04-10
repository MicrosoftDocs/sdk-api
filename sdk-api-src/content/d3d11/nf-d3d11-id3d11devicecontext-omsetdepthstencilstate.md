---
UID: NF:d3d11.ID3D11DeviceContext.OMSetDepthStencilState
title: ID3D11DeviceContext::OMSetDepthStencilState (d3d11.h)
author: windows-sdk-content
description: Sets the depth-stencil state of the output-merger stage.
old-location: direct3d11\id3d11devicecontext_omsetdepthstencilstate.htm
tech.root: direct3d11
ms.assetid: cd5642c4-8bbe-4b5d-9f04-87de82ee9601
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext interface [Direct3D 11],OMSetDepthStencilState method, ID3D11DeviceContext.OMSetDepthStencilState, ID3D11DeviceContext::OMSetDepthStencilState, OMSetDepthStencilState, OMSetDepthStencilState method [Direct3D 11], OMSetDepthStencilState method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::OMSetDepthStencilState, direct3d11.id3d11devicecontext_omsetdepthstencilstate, faf5401a-abab-bc40-9854-cf64f6ca05eb
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
 - ID3D11DeviceContext.OMSetDepthStencilState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::OMSetDepthStencilState


## -description


Sets the depth-stencil state of the output-merger stage.


## -parameters




### -param pDepthStencilState [in, optional]

Type: <b><a href="https://msdn.microsoft.com/cac22076-2ba6-4ab1-918e-8c9a7773acf6">ID3D11DepthStencilState</a>*</b>

Pointer to a depth-stencil state interface (see <a href="https://msdn.microsoft.com/cac22076-2ba6-4ab1-918e-8c9a7773acf6">ID3D11DepthStencilState</a>) to bind to the device. Set this to <b>NULL</b> to use the default state listed in <a href="https://msdn.microsoft.com/5e136ca8-8655-4c75-9bc0-bcf3a7af930a">D3D11_DEPTH_STENCIL_DESC</a>.


### -param StencilRef [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Reference value to perform against when doing a depth-stencil test. See remarks.


## -returns



Returns nothing.




## -remarks



To create a depth-stencil state interface, call <a href="https://msdn.microsoft.com/7577604c-922c-408c-8eab-2361ebda17df">ID3D11Device::CreateDepthStencilState</a>.

The method will hold a reference to the interfaces passed in.
      This differs from the device state behavior in Direct3D 10.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

