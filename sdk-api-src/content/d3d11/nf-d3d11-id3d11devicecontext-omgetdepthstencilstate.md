---
UID: NF:d3d11.ID3D11DeviceContext.OMGetDepthStencilState
title: ID3D11DeviceContext::OMGetDepthStencilState
author: windows-sdk-content
description: Gets the depth-stencil state of the output-merger stage.
old-location: direct3d11\id3d11devicecontext_omgetdepthstencilstate.htm
old-project: direct3d11
ms.assetid: d5ea53a8-62c9-46c9-96ed-8c9977d916b2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 46d0ab14-fdda-10ce-1e1a-4e551e1deeb3, ID3D11DeviceContext interface [Direct3D 11],OMGetDepthStencilState method, ID3D11DeviceContext.OMGetDepthStencilState, ID3D11DeviceContext::OMGetDepthStencilState, OMGetDepthStencilState, OMGetDepthStencilState method [Direct3D 11], OMGetDepthStencilState method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::OMGetDepthStencilState, direct3d11.id3d11devicecontext_omgetdepthstencilstate
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
 - ID3D11DeviceContext.OMGetDepthStencilState
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::OMGetDepthStencilState


## -description


Gets the depth-stencil state of the output-merger stage.


## -parameters




### -param ppDepthStencilState [out, optional]

Type: <b><a href="https://msdn.microsoft.com/cac22076-2ba6-4ab1-918e-8c9a7773acf6">ID3D11DepthStencilState</a>**</b>

Address of a pointer to a depth-stencil state interface (see <a href="https://msdn.microsoft.com/cac22076-2ba6-4ab1-918e-8c9a7773acf6">ID3D11DepthStencilState</a>) to be filled with information from the device.
          


### -param pStencilRef [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a>*</b>

Pointer to the stencil reference value used in the depth-stencil test.


## -returns



Returns nothing.




## -remarks



Any returned interfaces will have their reference count incremented by one. Applications should call IUnknown::Release on the returned interfaces when they are no longer needed to avoid memory leaks.

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

