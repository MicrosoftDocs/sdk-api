---
UID: NF:d2d1.DrawEllipse
title: DrawEllipse function
author: windows-sdk-content
description: Draws the outline of an ellipse with the specified dimensions and stroke.
old-location: direct2d\id2d1rendertarget_drawellipse.htm
old-project: direct2d
ms.assetid: dabbb399-2d72-41c3-8b2f-aea49d7ad0cb
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DrawEllipse, DrawEllipse methods [Direct2D], ID2D1RenderTarget::DrawEllipse, d2d1/DrawEllipse, direct2d.id2d1rendertarget_drawellipse
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: d2d1.h
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
req.typenames: D2D1_WINDOW_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget::DrawEllipse
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# DrawEllipse function


## -description


<span>Draws the outline of an ellipse with the specified dimensions and stroke.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3cd3aad6-72fc-41a3-a792-6ecac838c080">DrawEllipse(D2D1_ELLIPSE&,ID2D1Brush*,FLOAT,ID2D1StrokeStyle*)</a>
</td>
<td align="left" width="63%">
Draws the outline of the specified ellipse using the specified stroke style.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a760cc1e-4798-449d-bb45-693672d91132">DrawEllipse(D2D1_ELLIPSE*,ID2D1Brush*,FLOAT,ID2D1StrokeStyle*)</a>
</td>
<td align="left" width="63%">
Draws the outline of the specified ellipse using the specified stroke style.

</td>
</tr>
</table>

## -parameters


## -remarks



The <b>DrawEllipse</b> method doesn't return an error code if it fails. To determine whether a drawing operation (such as <b>DrawEllipse</b>) failed, check the result returned by the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a> or <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">ID2D1RenderTarget::Flush</a> methods. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/en-us/library/Dd756683(v=VS.85).aspx">How to Draw and Fill a Basic Shape</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd742849(v=VS.85).aspx">FillEllipse</a>



<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

