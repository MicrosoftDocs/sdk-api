---
UID: NF:d3d10.ID3D10Texture2D.Unmap
title: ID3D10Texture2D::Unmap
author: windows-sdk-content
description: Invalidate the pointer to the resource that was retrieved by ID3D10Texture2D::Map, and re-enable GPU access to the resource.
old-location: direct3d10\id3d10texture2d_unmap.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture2d_unmap.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D10Texture2D interface [Direct3D 10],Unmap method, ID3D10Texture2D.Unmap, ID3D10Texture2D::Unmap, Unmap, Unmap method [Direct3D 10], Unmap method [Direct3D 10],ID3D10Texture2D interface, d3d10/ID3D10Texture2D::Unmap, direct3d10.id3d10texture2d_unmap, e1ca6720-deda-a569-77bf-8e1b691dd284
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D10_USAGE
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Texture2D::Unmap


## -description


Invalidate the pointer to the resource that was retrieved by <a href="https://msdn.microsoft.com/40d0d246-bed9-48a2-9c00-68a5c58f49a5">ID3D10Texture2D::Map</a>, and re-enable GPU access to the resource.


## -parameters




### -param Subresource [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


<a href="https://msdn.microsoft.com/c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69">Subresource</a> to be unmapped. See <a href="https://msdn.microsoft.com/48079797-b5c8-487b-a343-a5623b780350">D3D10CalcSubresource</a> for more details.


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




<a href="https://msdn.microsoft.com/87e9a9ee-7e73-4f3c-8898-c8bbfe6508c2">ID3D10Texture2D Interface</a>
 

 

