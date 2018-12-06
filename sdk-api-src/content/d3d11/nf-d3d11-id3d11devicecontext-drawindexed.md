---
UID: NF:d3d11.ID3D11DeviceContext.DrawIndexed
title: ID3D11DeviceContext::DrawIndexed
author: windows-sdk-content
description: Draw indexed, non-instanced primitives.
old-location: direct3d11\id3d11devicecontext_drawindexed.htm
tech.root: direct3d11
ms.assetid: 461a64ec-f3e6-4f6a-8bc4-a349d19501a8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 45129747-420c-37ba-aae0-05275af46932, DrawIndexed, DrawIndexed method [Direct3D 11], DrawIndexed method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],DrawIndexed method, ID3D11DeviceContext.DrawIndexed, ID3D11DeviceContext::DrawIndexed, d3d11/ID3D11DeviceContext::DrawIndexed, direct3d11.id3d11devicecontext_drawindexed
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
 - ID3D11DeviceContext.DrawIndexed
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext::DrawIndexed


## -description


Draw indexed, non-instanced primitives.


## -parameters




### -param IndexCount [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of indices to draw.


### -param StartIndexLocation [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The location of the first index read by the GPU from the index buffer.


### -param BaseVertexLocation [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

A value added to each index before reading a vertex from the vertex buffer.


## -returns



Returns nothing.




## -remarks



A draw API submits work to the rendering pipeline.

If the sum of both indices is negative, the result of the function call is undefined.




## -see-also




<a href="https://msdn.microsoft.com/afb32c09-77f2-4c33-bd93-8dce92a2e45e">ID3D11DeviceContext</a>
 

 

