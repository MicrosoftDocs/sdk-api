---
UID: NN:d2d1_3.ID2D1GradientMesh
title: ID2D1GradientMesh
author: windows-sdk-content
description: Represents a device-dependent representation of a gradient mesh composed of patches. Use the ID2D1DeviceContext2::CreateGradientMesh method to create an instance of ID2D1GradientMesh.
old-location: direct2d\id2d1gradientmesh.htm
tech.root: direct2d
ms.assetid: 0c51da97-7b70-d828-2a4d-cb62ff378a56
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ID2D1GradientMesh, ID2D1GradientMesh interface [Direct2D], ID2D1GradientMesh interface [Direct2D],described, d2d1_3/ID2D1GradientMesh, direct2d.id2d1gradientmesh
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - ID2D1GradientMesh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1GradientMesh interface


## -description


Represents a device-dependent representation of a gradient mesh composed of patches. 
  Use the <a href="https://msdn.microsoft.com/7c471ba3-fb0f-b735-d10b-9d0a56b32863">ID2D1DeviceContext2::CreateGradientMesh method</a> to create an instance of ID2D1GradientMesh.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1GradientMesh</b> interface inherits from <a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>. <b>ID2D1GradientMesh</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1GradientMesh</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/389bc25d-832c-56de-3568-d136f60b935f">GetPatchCount</a>
</td>
<td align="left" width="63%">
Returns the number of patches that make up this gradient mesh.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3ef9370-fb9f-d55b-d910-7dd938ecf0b6">GetPatches</a>
</td>
<td align="left" width="63%">
Returns a subset of the patches that make up this gradient mesh.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8f19e74a-f010-4082-a4da-d1dc3cfe3192">ID2D1Resource</a>
 

 

