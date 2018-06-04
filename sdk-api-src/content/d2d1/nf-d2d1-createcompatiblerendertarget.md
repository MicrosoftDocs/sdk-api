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

# CreateCompatibleRenderTarget function


## -description


<span>Creates a new  bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target .
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/043d18f4-0cf6-47eb-9a1e-aa676a947bd6">CreateCompatibleRenderTarget(D2D1_SIZE_F,D2D1_SIZE_U,D2D1_PIXEL_FORMAT,D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS,ID2D1BitmapRenderTarget**)</a>
</td>
<td align="left" width="63%">

    Creates a bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a276af2d-b9bf-465b-86cf-f5bc27c3447f">CreateCompatibleRenderTarget(D2D1_SIZE_F*,D2D1_SIZE_U*,D2D1_PIXEL_FORMAT*,D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS,ID2D1BitmapRenderTarget**)</a>
</td>
<td align="left" width="63%">
Creates a bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target. 

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e36fbf45-9827-4ea0-ac52-676ba826a7d3">CreateCompatibleRenderTarget(ID2D1BitmapRenderTarget**)</a>
</td>
<td align="left" width="63%">

    Creates a new  bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target and has the same size, DPI, and pixel format (but not alpha mode) as the current render target.  

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8687186-abea-4412-83f7-b0d89b453d9d">CreateCompatibleRenderTarget(D2D1_SIZE_F,ID2D1BitmapRenderTarget**)</a>
</td>
<td align="left" width="63%">
Creates a new  bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target and has the same pixel format (but not alpha mode) as the current render target.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/948f9ab7-22d4-427c-9b48-fe0a018b9626">CreateCompatibleRenderTarget(D2D1_SIZE_F,D2D1_SIZE_U,ID2D1BitmapRenderTarget**)</a>
</td>
<td align="left" width="63%">
Creates a bitmap render target for use during intermediate off-screen drawing that is compatible with the current render target. The new bitmap render target has the same pixel format (but not alpha mode) as the current render target.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a80f460-56b2-4049-9de9-8fcde06c063c">CreateCompatibleRenderTarget(D2D1_SIZE_F,D2D1_SIZE_U,D2D1_PIXEL_FORMAT,ID2D1BitmapRenderTarget**)</a>
</td>
<td align="left" width="63%">
Creates a bitmap render target for use during intermediate offscreen drawing that is compatible with the current render target.

</td>
</tr>
</table>

## -parameters


## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

