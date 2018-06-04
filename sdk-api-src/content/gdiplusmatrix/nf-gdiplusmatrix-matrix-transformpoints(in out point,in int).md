---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# Matrix::TransformPoints(IN OUT Point,IN INT)


## -description


<span>This topic lists the TransformPoints methods of the <a href="https://msdn.microsoft.com/92b0d9db-3d4c-47b8-87cd-60d7b4323f0a">Matrix</a> class. For a complete list of methods for the <b>Matrix</b> class, see <a href="https://msdn.microsoft.com/d43a7956-9822-4093-9722-91f0d2edf50c">Matrix Methods</a>. 
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b9bd7c2-a773-4957-81f7-c4a501b52b8f">TransformPoints(Point*,INT)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/6b9bd7c2-a773-4957-81f7-c4a501b52b8f">Matrix::TransformPoints</a> method multiplies each point in an array by this matrix. Each point is treated as a row matrix. The multiplication is performed with the row matrix on the left and this matrix on the right.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2cabdfe3-e222-4afb-99c5-201e87b4c24e">TransformPoints(PointF*,INT)</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/2cabdfe3-e222-4afb-99c5-201e87b4c24e">Matrix::TransformPoints</a> method multiplies each point in an array by this matrix. Each point is treated as a row matrix. The multiplication is performed with the row matrix on the left and this matrix on the right.

</td>
</tr>
</table>

## -parameters

