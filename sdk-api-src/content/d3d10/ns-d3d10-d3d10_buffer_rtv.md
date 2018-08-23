---
UID: NS:d3d10.D3D10_BUFFER_RTV
title: D3D10_BUFFER_RTV
author: windows-sdk-content
description: Specifies the elements from a buffer resource to use in a render-target view.
old-location: direct3d10\d3d10_buffer_rtv.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_buffer_rtv.htm
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: 4eb8f5a5-bb65-b551-7e42-ac051b09f97c, D3D10_BUFFER_RTV, D3D10_BUFFER_RTV structure [Direct3D 10], d3d10/D3D10_BUFFER_RTV, direct3d10.d3d10_buffer_rtv
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: d3d10.h
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
req.typenames: D3D10_BUFFER_RTV
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_BUFFER_RTV
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D10_BUFFER_RTV structure


## -description


Specifies the elements from a <a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">buffer</a> resource to use in a render-target view.


## -struct-fields




### -field FirstElement

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Number of bytes between the beginning of the buffer and the first element to access.


### -field ElementOffset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The offset of the first element in the view to access, relative to element 0.


### -field NumElements

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The total number of elements in the view.


### -field ElementWidth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The width of each element (in bytes). This can be determined from the format stored in the render-target-view description.


## -remarks



A render-target view is a member of a render-target-view description (see <a href="https://msdn.microsoft.com/en-us/library/Bb172410(v=VS.85).aspx">D3D10_RENDER_TARGET_VIEW_DESC</a>). Create a render-target view by calling <a href="https://msdn.microsoft.com/en-us/library/Bb173556(v=VS.85).aspx">ID3D10Device::CreateRenderTargetView</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb205277(v=VS.85).aspx">Resource Structures</a>
 

 

