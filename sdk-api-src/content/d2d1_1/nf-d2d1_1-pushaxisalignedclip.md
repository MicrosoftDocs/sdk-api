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

# PushAxisAlignedClip function


## -description


<span>Specifies a rectangle to which all subsequent drawing operations are clipped.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6a0743c-e964-41f5-807f-541f00f552b5">PushAxisAlignedClip(D2D1_RECT_F&,D2D1_ANTIALIAS_MODE)</a>
</td>
<td align="left" width="63%">
Specifies a rectangle to which all subsequent drawing operations are clipped.
    

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db2e975e-e5c5-4c57-8071-ec042b9a6fb9">PushAxisAlignedClip(D2D1_RECT_F*,D2D1_ANTIALIAS_MODE)</a>
</td>
<td align="left" width="63%">
Specifies a rectangle to which all subsequent drawing operations are clipped.

</td>
</tr>
</table>

## -parameters


## -remarks



A           <a href="https://msdn.microsoft.com/a6a0743c-e964-41f5-807f-541f00f552b5">PushAxisAlignedClip</a> and <a href="https://msdn.microsoft.com/0f0a2826-2356-4ced-a372-5bb59dd394ee">PopAxisAlignedClip</a> pair can occur around or within a <a href="https://msdn.microsoft.com/9336662c-e94e-40ba-adbe-066d704958bc">PushLayer</a> and <a href="https://msdn.microsoft.com/6ab05160-4f42-477f-a5bf-f16863b0635c">PopLayer</a>, but cannot overlap. For example, the sequence of <b>PushAxisAlignedClip</b>, <a href="https://msdn.microsoft.com/905e9c76-d09e-4df8-8343-520d856ec6b8">PushLayer</a>, <b>PopLayer</b>, <b>PopAxisAlignedClip</b> is valid, but the sequence of <b>PushAxisAlignedClip</b>, <b>PushLayer</b>, <b>PopAxisAlignedClip</b>, <b>PopLayer</b> is invalid.

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>PushAxisAlignedClip</b>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 


#### Examples

For an example, see the <a href="https://msdn.microsoft.com/4196653a-9177-4a41-9db9-4738a41313aa">How to Clip with an Axis-Aligned Clip Rectangle</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

