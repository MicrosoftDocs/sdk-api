---
UID: NF:d3d10.ID3D10Texture2D.Unmap
title: ID3D10Texture2D::Unmap
author: windows-sdk-content
description: Invalidate the pointer to the resource that was retrieved by ID3D10Texture2D::Map, and re-enable GPU access to the resource.
old-location: direct3d10\id3d10texture2d_unmap.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture2d_unmap.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D10Texture2D interface [Direct3D 10],Unmap method, ID3D10Texture2D.Unmap, ID3D10Texture2D::Unmap, Unmap, Unmap method [Direct3D 10], Unmap method [Direct3D 10],ID3D10Texture2D interface, d3d10/ID3D10Texture2D::Unmap, direct3d10.id3d10texture2d_unmap, e1ca6720-deda-a569-77bf-8e1b691dd284
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ID3D10Texture2D.Unmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d3d10.h
: 
- ID3D10Texture2D.Unmap
: 
---

# ID3D10Texture2D::Unmap


## -description


Invalidate the pointer to the resource that was retrieved by <a href="https://msdn.microsoft.com/en-us/library/Bb173869(v=VS.85).aspx">ID3D10Texture2D::Map</a>, and re-enable GPU access to the resource.


## -parameters




### -param Subresource [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>


<a href="https://msdn.microsoft.com/en-us/library/Bb205133(v=VS.85).aspx">Subresource</a> to be unmapped. See <a href="https://msdn.microsoft.com/en-us/library/Bb694525(v=VS.85).aspx">D3D10CalcSubresource</a> for more details.


## -returns



Returns nothing.




## -remarks



A subresource must be mapped before Unmap is called.

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

Unmap in Direct3D 10 is analogous to resource Unlock in Direct3D 9.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173867(v=VS.85).aspx">ID3D10Texture2D Interface</a>
 

 

