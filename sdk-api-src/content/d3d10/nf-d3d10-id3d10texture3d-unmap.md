---
UID: NF:d3d10.ID3D10Texture3D.Unmap
title: ID3D10Texture3D::Unmap (d3d10.h)
author: windows-sdk-content
description: Invalidate the pointer to the resource retrieved by ID3D10Texture3D::Map, and re-enable the GPU's access to the resource.
old-location: direct3d10\id3d10texture3d_unmap.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture3d_unmap.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D10Texture3D interface [Direct3D 10],Unmap method, ID3D10Texture3D.Unmap, ID3D10Texture3D::Unmap, Unmap, Unmap method [Direct3D 10], Unmap method [Direct3D 10],ID3D10Texture3D interface, c26b8025-823a-b16b-6cb8-9316b5866e7e, d3d10/ID3D10Texture3D::Unmap, direct3d10.id3d10texture3d_unmap
ms.topic: method
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
 - ID3D10Texture3D.Unmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Texture3D::Unmap


## -description


Invalidate the pointer to the resource retrieved by <a href="https://msdn.microsoft.com/en-us/library/Bb173873(v=VS.85).aspx">ID3D10Texture3D::Map</a>, and re-enable the GPU's access to the resource.


## -parameters




### -param Subresource [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">Subresource</a> to be unmapped. See <a href="https://msdn.microsoft.com/en-us/library/Bb694525(v=VS.85).aspx">D3D10CalcSubresource</a> for more details.


## -returns



Returns nothing.




## -remarks



A subresource must be mapped before Unmap is called.

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

Unmap() in Direct3D 10 is analogous to resource Unlock() in Direct3D 9.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173871(v=VS.85).aspx">ID3D10Texture3D Interface</a>
 

 

