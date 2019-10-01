---
UID: NF:d3d11.ID3D11DeviceContext.DrawIndexedInstancedIndirect
title: ID3D11DeviceContext::DrawIndexedInstancedIndirect (d3d11.h)
author: windows-sdk-content
description: Draw indexed, instanced, GPU-generated primitives.
old-location: direct3d11\id3d11devicecontext_drawindexedinstancedindirect.htm
tech.root: direct3d11
ms.assetid: c6969210-b452-4a49-a3d7-d849b1d2ebb5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 490eea55-c4b9-bcfb-1fd8-021b92e7979d, DrawIndexedInstancedIndirect, DrawIndexedInstancedIndirect method [Direct3D 11], DrawIndexedInstancedIndirect method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],DrawIndexedInstancedIndirect method, ID3D11DeviceContext.DrawIndexedInstancedIndirect, ID3D11DeviceContext::DrawIndexedInstancedIndirect, d3d11/ID3D11DeviceContext::DrawIndexedInstancedIndirect, direct3d11.id3d11devicecontext_drawindexedinstancedindirect
ms.topic: method
f1_keywords: 
 - "d3d11/ID3D11DeviceContext.DrawIndexedInstancedIndirect"
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
 - ID3D11DeviceContext.DrawIndexedInstancedIndirect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11DeviceContext::DrawIndexedInstancedIndirect


## -description


Draw indexed, instanced, GPU-generated primitives.


## -parameters




### -param pBufferForArgs [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>, which is a buffer containing the GPU generated primitives.
          


### -param AlignedByteOffsetForArgs [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Offset in <i>pBufferForArgs</i> to the start of the GPU generated primitives.
          


## -returns



Returns nothing.




## -remarks



When an application creates a buffer that is associated with the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a> interface that  <i>pBufferForArgs</i> points to, the application must set the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ne-d3d11-d3d11_resource_misc_flag">D3D11_RESOURCE_MISC_DRAWINDIRECT_ARGS</a> flag in the <b>MiscFlags</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ns-d3d11-d3d11_buffer_desc">D3D11_BUFFER_DESC</a> structure that describes the buffer. To create the buffer, the application calls the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createbuffer">ID3D11Device::CreateBuffer</a> method and in this call passes a pointer to <b>D3D11_BUFFER_DESC</b> in the <i>pDesc</i> parameter.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
 

 

