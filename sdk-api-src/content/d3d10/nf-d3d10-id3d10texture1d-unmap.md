---
UID: NF:d3d10.ID3D10Texture1D.Unmap
title: ID3D10Texture1D::Unmap
author: windows-sdk-content
description: Invalidate the pointer to a resource that was retrieved by ID3D10Texture1D::Map, and re-enable the GPU's access to that resource.
old-location: direct3d10\id3d10texture1d_unmap.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture1d_unmap.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 19252c0c-8539-ab86-d402-c4d9d235f30e, ID3D10Texture1D interface [Direct3D 10],Unmap method, ID3D10Texture1D.Unmap, ID3D10Texture1D::Unmap, Unmap, Unmap method [Direct3D 10], Unmap method [Direct3D 10],ID3D10Texture1D interface, d3d10/ID3D10Texture1D::Unmap, direct3d10.id3d10texture1d_unmap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - ID3D10Texture1D.Unmap
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Texture1D::Unmap


## -description


Invalidate the pointer to a resource that was retrieved by <a href="https://msdn.microsoft.com/ff11d7a7-2e9a-4220-9aa2-c9a96355cc0d">ID3D10Texture1D::Map</a>, and re-enable the GPU's access to that resource.


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




<a href="https://msdn.microsoft.com/d73cdd85-d6e2-4724-a069-6a4edb5b354e">ID3D10Texture1D Interface</a>
 

 

