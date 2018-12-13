---
UID: NF:d2d1.ID2D1RenderTarget.PushAxisAlignedClip
title: ID2D1RenderTarget::PushAxisAlignedClip
author: windows-sdk-content
description: Specifies a rectangle to which all subsequent drawing operations are clipped.
old-location: direct2d\id2d1rendertarget_pushaxisalignedclip.htm
tech.root: direct2d
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID2D1RenderTarget.PushAxisAlignedClip, ID2D1RenderTarget::PushAxisAlignedClip, PushAxisAlignedClip, PushAxisAlignedClip methods [Direct2D], d2d1_1/PushAxisAlignedClip, direct2d.id2d1rendertarget_pushaxisalignedclip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: D2d1.h
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget::PushAxisAlignedClip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::PushAxisAlignedClip


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



A           <a href="https://msdn.microsoft.com/a6a0743c-e964-41f5-807f-541f00f552b5">PushAxisAlignedClip</a> and <a href="https://msdn.microsoft.com/0f0a2826-2356-4ced-a372-5bb59dd394ee">PopAxisAlignedClip</a> pair can occur around or within a <a href="https://msdn.microsoft.com/en-us/library/Dd742856(v=VS.85).aspx">PushLayer</a> and <a href="https://msdn.microsoft.com/6ab05160-4f42-477f-a5bf-f16863b0635c">PopLayer</a>, but cannot overlap. For example, the sequence of <b>PushAxisAlignedClip</b>, <a href="https://msdn.microsoft.com/905e9c76-d09e-4df8-8343-520d856ec6b8">PushLayer</a>, <b>PopLayer</b>, <b>PopAxisAlignedClip</b> is valid, but the sequence of <b>PushAxisAlignedClip</b>, <b>PushLayer</b>, <b>PopAxisAlignedClip</b>, <b>PopLayer</b> is invalid.

This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>PushAxisAlignedClip</b>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 


#### Examples

For an example, see the <a href="https://msdn.microsoft.com/4196653a-9177-4a41-9db9-4738a41313aa">How to Clip with an Axis-Aligned Clip Rectangle</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

