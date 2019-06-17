---
UID: NF:d3d10.ID3D10Device.ClearDepthStencilView
title: ID3D10Device::ClearDepthStencilView (d3d10.h)
author: windows-sdk-content
description: Clears the depth-stencil resource.
old-location: direct3d10\id3d10device_cleardepthstencilview.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_cleardepthstencilview.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 35b5c5f1-9875-7367-51bd-ef0f9a3ea798, ClearDepthStencilView, ClearDepthStencilView method [Direct3D 10], ClearDepthStencilView method [Direct3D 10],ID3D10Device interface, ID3D10Device interface [Direct3D 10],ClearDepthStencilView method, ID3D10Device.ClearDepthStencilView, ID3D10Device::ClearDepthStencilView, d3d10/ID3D10Device::ClearDepthStencilView, direct3d10.id3d10device_cleardepthstencilview
ms.topic: method
f1_keywords: ["d3d10/ID3D10Device.ClearDepthStencilView"]
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.ClearDepthStencilView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Device::ClearDepthStencilView


## -description


Clears the depth-stencil resource.


## -parameters




### -param pDepthStencilView [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10depthstencilview">ID3D10DepthStencilView</a>*</b>

Pointer to the depth stencil to be cleared.


### -param ClearFlags [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Which parts of the buffer to clear. See <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ne-d3d10-d3d10_clear_flag">D3D10_CLEAR_FLAG</a>.


### -param Depth [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Clear the depth buffer with this value. This value will be clamped between 0 and 1.


### -param Stencil [in]

Type: <b>UINT8</b>

Clear the stencil buffer with this value.


## -returns



Returns nothing.




## -remarks



<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

Unlike Direct3D 9, the full extent of the resource view is always cleared. Viewport and scissor settings are not applied.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
 

 

