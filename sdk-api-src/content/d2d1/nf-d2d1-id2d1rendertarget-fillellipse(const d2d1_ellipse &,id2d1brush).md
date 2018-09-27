---
UID: NF:d2d1.ID2D1RenderTarget.FillEllipse(const D2D1_ELLIPSE &,ID2D1Brush)
title: ID2D1RenderTarget::FillEllipse(const D2D1_ELLIPSE &,ID2D1Brush)
author: windows-sdk-content
description: Paints the interior of the specified ellipse.
old-location: direct2d\id2d1rendertarget_fillellipse.htm
tech.root: direct2d
ms.assetid: 149fb303-d2e8-416c-b28f-8bc5f1482ba6
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: FillEllipse, FillEllipse methods [Direct2D], ID2D1RenderTarget.FillEllipse, ID2D1RenderTarget.FillEllipse(const D2D1_ELLIPSE &,ID2D1Brush), ID2D1RenderTarget::FillEllipse, ID2D1RenderTarget::FillEllipse(const D2D1_ELLIPSE &,ID2D1Brush), d2d1/FillEllipse, direct2d.id2d1rendertarget_fillellipse
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
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
 - ID2D1RenderTarget::FillEllipse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::FillEllipse(const D2D1_ELLIPSE &,ID2D1Brush)


## -description


<span>Paints the interior of the specified ellipse.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/007c5733-91d4-42c8-bd76-ae10225d3d5e">FillEllipse(D2D1_ELLIPSE&,ID2D1Brush*)</a>
</td>
<td align="left" width="63%">
Paints the interior of the specified ellipse.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30027ffd-f835-44a7-8c58-c8cef79f0037">FillEllipse(D2D1_ELLIPSE*,ID2D1Brush*)</a>
</td>
<td align="left" width="63%">
Paints the interior of the specified ellipse.

</td>
</tr>
</table>

## -parameters


## -remarks



This method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>FillEllipse</b>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/8a68fc3f-118c-447b-856c-05417ae4ef29">How to Draw and Fill a Basic Shape</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/8a68fc3f-118c-447b-856c-05417ae4ef29">How to Draw and Fill a Basic Shape</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

