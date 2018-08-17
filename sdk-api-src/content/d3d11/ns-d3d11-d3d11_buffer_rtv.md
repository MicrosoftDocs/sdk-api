---
UID: NS:d3d11.D3D11_BUFFER_RTV
title: D3D11_BUFFER_RTV
author: windows-sdk-content
description: Specifies the elements in a buffer resource to use in a render-target view.
old-location: direct3d11\d3d11_buffer_rtv.htm
old-project: direct3d11
ms.assetid: 979c69cf-f9b5-4b10-92ff-ad5245880802
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 89ee8333-dedf-139c-e1a8-05365866ee34, D3D11_BUFFER_RTV, D3D11_BUFFER_RTV structure [Direct3D 11], d3d11/D3D11_BUFFER_RTV, direct3d11.d3d11_buffer_rtv
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d11.h
req.include-header: 
req.redist: 
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
req.typenames: D3D11_BUFFER_RTV
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_BUFFER_RTV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D11_BUFFER_RTV structure


## -description


Specifies the elements in a buffer resource to use in a render-target view.


## -struct-fields




### -field FirstElement

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Number of bytes between the beginning of the buffer and the first element to access.
            


### -field ElementOffset

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The offset of the first element in the view to access, relative to element 0.
            


### -field NumElements

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The total number of elements in the view.
            


### -field ElementWidth

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

The width of each element (in bytes). This can be determined from the format stored in the render-target-view description.
            


## -remarks



A render-target view is a member of a render-target-view description (see <a href="https://msdn.microsoft.com/en-us/library/Ff476201(v=VS.85).aspx">D3D11_RENDER_TARGET_VIEW_DESC</a>). Create a render-target view by calling <a href="https://msdn.microsoft.com/en-us/library/Ff476517(v=VS.85).aspx">ID3D11Device::CreateRenderTargetView</a>.
        




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476173(v=VS.85).aspx">Resource Structures</a>
 

 

