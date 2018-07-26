---
UID: NF:d3d11.ID3D11DeviceContext.RSSetScissorRects
title: ID3D11DeviceContext::RSSetScissorRects
author: windows-sdk-content
description: Bind an array of scissor rectangles to the rasterizer stage.
old-location: direct3d11\id3d11devicecontext_rssetscissorrects.htm
old-project: direct3d11
ms.assetid: 80bee89d-1743-475c-a284-8137cfacdac2
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: 28026545-0d38-beff-91cf-a929caef1657, ID3D11DeviceContext interface [Direct3D 11],RSSetScissorRects method, ID3D11DeviceContext.RSSetScissorRects, ID3D11DeviceContext::RSSetScissorRects, RSSetScissorRects, RSSetScissorRects method [Direct3D 11], RSSetScissorRects method [Direct3D 11],ID3D11DeviceContext interface, d3d11/ID3D11DeviceContext::RSSetScissorRects, direct3d11.id3d11devicecontext_rssetscissorrects
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
 - ID3D11DeviceContext.RSSetScissorRects
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext::RSSetScissorRects


## -description


Bind an array of scissor rectangles to the rasterizer stage.


## -parameters




### -param NumRects [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of scissor rectangles to bind.


### -param pRects [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/d1cbbbd7-1221-4706-b805-8422c5ebdadc">D3D11_RECT</a>*</b>

An array of scissor rectangles (see <a href="https://msdn.microsoft.com/d1cbbbd7-1221-4706-b805-8422c5ebdadc">D3D11_RECT</a>).
          


## -returns



Returns nothing.




## -remarks



All scissor rects must be set atomically as one operation. Any scissor rects not defined by the call are disabled.

The scissor rectangles will only be used if ScissorEnable is set to true in the rasterizer state (see <a href="https://msdn.microsoft.com/53252fef-f557-46d1-b6a7-ccc8a059752a">D3D11_RASTERIZER_DESC</a>).
        

Which scissor rectangle to use is determined by the SV_ViewportArrayIndex semantic output by a geometry shader (see shader semantic syntax). If a geometry shader does not make use of the SV_ViewportArrayIndex semantic then Direct3D will use the first scissor rectangle in the array.

Each scissor rectangle in the array corresponds to a viewport in an array of viewports (see <a href="https://msdn.microsoft.com/7326e9a8-edfa-4e5a-a29e-fe7c54a055f5">ID3D11DeviceContext::RSSetViewports</a>).
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

