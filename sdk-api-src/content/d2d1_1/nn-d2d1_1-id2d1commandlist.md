---
UID: NN:d2d1_1.ID2D1CommandList
title: ID2D1CommandList (d2d1_1.h)
description: Represents a sequence of commands that can be recorded and played back.
helpviewer_keywords: ["ID2D1CommandList","ID2D1CommandList interface [Direct2D]","ID2D1CommandList interface [Direct2D]","described","d2d1_1/ID2D1CommandList","direct2d.id2d1commandlist"]
old-location: direct2d\id2d1commandlist.htm
tech.root: Direct2D
ms.assetid: 30b89f53-d20b-4070-abcd-ef95813130d1
ms.date: 12/05/2018
ms.keywords: ID2D1CommandList, ID2D1CommandList interface [Direct2D], ID2D1CommandList interface [Direct2D],described, d2d1_1/ID2D1CommandList, direct2d.id2d1commandlist
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1CommandList
 - d2d1_1/ID2D1CommandList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1CommandList
---

# ID2D1CommandList interface


## -description

Represents a sequence of commands that can be recorded and played back.

## -inheritance

The <b>ID2D1CommandList</b> interface inherits from <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>. <b>ID2D1CommandList</b> also has these types of members:

## -remarks

The command list does not include static copies of resources with the recorded set of commands. All bitmaps, effects, and geometries are stored as references to the actual resource and all the brushes are stored by value. All the resource creation and destruction happens outside of the command list. The following table lists resources and how they are treated inside of a command list.

<table>
<tr>
<th>Resource</th>
<th>How it is treated by the command list</th>
</tr>
<tr>
<td>Solid-color brush</td>
<td>Passed by value.</td>
</tr>
<tr>
<td>Bitmap brush</td>
<td>The brush is passed by value but the bitmap that is used to create the brush is in fact referenced.</td>
</tr>
<tr>
<td>Gradient brushes – both linear and radial gradient</td>
<td>The brush is passed by value but the gradient stop collection itself is referenced. The gradient stop collection object is immutable. </td>
</tr>
<tr>
<td>Bitmaps</td>
<td>Passed by reference.</td>
</tr>
<tr>
<td>Drawing state block</td>
<td>The actual state on the device context is converted into set functions like set transform and is passed by value.</td>
</tr>
<tr>
<td>Geometry</td>
<td>Immutable object passed by value.</td>
</tr>
<tr>
<td>Stroke style</td>
<td>Immutable object passed by value.</td>
</tr>
<tr>
<td>Mesh</td>
<td>Immutable object passed by value.</td>
</tr>
</table>
 

<h3><a id="Using_a_CommandList_as_a_Target"></a><a id="using_a_commandlist_as_a_target"></a><a id="USING_A_COMMANDLIST_AS_A_TARGET"></a>Using a CommandList as a Target</h3>
The following pseudocode illustrates the different cases where a target is set as either a command list or as a bitmap.


``` syntax
//create a D2D device from an already created DXGI device 
ID2D1Device *pD2D1Device;
pD2D1Factory->CreateDevice(pDxgiDevice, &pD2D1Device);

//create a D2D device context from the D2D device
ID2D1DeviceContext *pD2D1DeviceContext;
pD2D1Device->CreateD2D1DeviceContext(&pD2D1DeviceContext);

//create command list
ID2D1CommandList *pCommandList1;
pD2D1DeviceContext->CreateCommandList(&pCommandList1);

//CreateBitmap
ID2D1Bitmap *pBitmap1;
ID2D1Bitmap *pBitmap2;
pD2D1DeviceContext->CreateBitmap(…, &pBitmap1);
pD2D1DeviceContext->CreateBitmap(…, &pBitmap2);

//Set the bitmap as the target
pD2D1DeviceContext->SetTarget(pBitmap1);
pD2D1DeviceContext->BeginDraw();
RenderMyVectorContent(pD2D1DeviceContext);
pD2D1DeviceContext->EndDraw();

//Set the command list as the target
pD2D1DeviceContext->SetTarget(pCommandList1);
pD2D1DeviceContext->BeginDraw();
RenderMyVectorContent(pD2D1DeviceContext);
pD2D1DeviceContext->EndDraw();

//Drawing a command list to a bitmap target
pD2D1DeviceContext->SetTarget(pBitmap2);
pD2D1DeviceContext->BeginDraw();
pD2D1DeviceContext->DrawImage(pCommandList1);
pD2D1DeviceContext->EndDraw();
```

<ul>
<li><b>Set the bitmap as the target:</b>In this case, all contents rendered to the bitmap are rasterized. If this bitmap is used somewhere else, it will not be resolution independent and if a transformation like <a href="/windows/desktop/Direct2D/high-quality-scale">High Quality Scale</a> is used, it will not maintain fidelity.</li>
<li><b>Set the command list as the target:</b>In this case, instead of the scene being rasterized, all of the commands are recorded. When the command list is used later for screen drawing using <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1effect_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)">ID2D1DeviceContext::DrawImage</a> or passed to an XPS print control, the vector content is replayed with no loss of fidelity.</li>
<li><b>Drawing a command list to a bitmap target:</b>In this case because the target is a bitmap, the command list is drawn to the bitmap and is no longer resolution independent.</li>
</ul>
The only way to retain vector content for later playback with full fidelity is to set the target type as a command list. When a bitmap is set as a target, any drawing on that target will get rasterized.

<h3><a id="Using_a_CommandList_to_Create_a_Brush"></a><a id="using_a_commandlist_to_create_a_brush"></a><a id="USING_A_COMMANDLIST_TO_CREATE_A_BRUSH"></a>Using a CommandList to Create a Brush</h3>
Command lists are a good way to support pattern brushes, because they are capable of retaining fidelity on replay. The desired pattern can be stored as a command list, which can be used to create an image brush. This brush can then be used to paint paths.

The type of brush that supports filling a path with a command list is called an <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1imagebrush">image brush</a>.

The following psuedocode illustrates the process of using a command list with an image brush.
``` syntax
//Draw the pattern to the command list
ID2D1CommandList *pCommandList;
pD2D1DeviceContext->SetTarget(pCommandList);
pD2D1DeviceContext->BeginDraw();
DrawMyPattern(pD2D1DeviceContext);
pD2D1DeviceContext->EndDraw();

//Create the image brush from the command list
ID2D1ImageBrush *pImageBrush;
pD2D1DeviceContext->CreateImageBrush(
    pCommandList, 
    pImageBrushProperties,
    pBrushProperties,
    &pImageBrush);

//Fill the ellipse with the pattern brush
pD2D1DeviceContext->SetTarget(pTargetBitmap);
pD2D1DeviceContext->BeginDraw();
pD2D1DeviceContext->FillEllipse(pEllipse, pImageBrush);
pD2D1DeviceContext->EndDraw();

```
Because the brush accepts an image, it has the following other benefits as well:<ul>
<li>Because the output of an effect graph is an image, this image can be used to create an image brush, which effectively provides the capability of using an effect as a fill.</li>
<li>Because the command list is a type of image, vector content can be inserted into an effect graph and can also be tiled or operated on. For example, a large copyright notice can be inserted over a graph with a virtualized image and then encoded.</li>
</ul>


<h3><a id="Using_a_CommandList_as_a_Replacement_for_a_Compatible_Render_Target"></a><a id="using_a_commandlist_as_a_replacement_for_a_compatible_render_target"></a><a id="USING_A_COMMANDLIST_AS_A_REPLACEMENT_FOR_A_COMPATIBLE_RENDER_TARGET"></a>Using a CommandList as a Replacement for a Compatible Render Target</h3>
Compatible render targets are used very often for off-screen rendering to an intermediate bitmap that is later composited with the actual scene. Especially in the case of printing, using compatible render targets will increase the memory footprint because everything will be rasterized and sent to XPS instead of retaining the actual primitives. In this scenario, a developer is better off replacing the compatible render target with an intermediate command list. 
The following pseudo code illustrates this point.


``` syntax
pD2D1Device->CreateDeviceContext(&pD2D1DeviceContext);
pRenderTarget->CreateCompatibleRenderTarget(…, &pCompatibleRenderTarget);

//render to the compatible render target
pCompatibleRenderTarget->BeginDraw();
RenderMyScene1(pCompatibleRenderTarget);
pCompatibleRenderTarget->EndDraw();

//get the bitmap from the compatible render target
pCompatibleRenderTarget->GetBitmap(pCompatBitmap);

//draw this bitmap on the device context
pD2D1DeviceContext->SetTarget(pTargetBitmap)
pD2D1DeviceContext->BeginDraw();
pD2D1DeviceContext->DrawBitmap(pCompatBitmap);
pD2D1DeviceContext->EndDraw();

//draw something else on the compatible render target
pCompatibleRenderTarget->BeginDraw();
pCompatibleRenderTarget->Clear();
pCompatibleRenderTarget->RenderScene2();
pCompatibleRenderTarget->EndDraw();

//get the bitmap from the compatible render target
pCompatibleRenderTarget->GetBitmap(pCompatBitmap);

//draw this bitmap on the device context
pD2D1DeviceContext->SetTarget(pTargetBitmap)
pD2D1DeviceContext->BeginDraw();
pD2D1DeviceContext->DrawBitmap(pCompatBitmap);
pD2D1DeviceContext->EndDraw();


//Use a command list instead for better quality and performance 

//store the original target
pOriginalTarget = pD2D1DeviceContext->GetTarget();

pD2D1DeviceContext->CreateCommandList(pCommandList1);

//draw to command list 1
pD2D1DeviceContext->SetTarget(pCommandList1);
pD2D1DeviceContext->BeginDraw();
RenderMyScene1(pD2D1DeviceContext);
pD2D1DeviceContext->EndDraw();

//draw the command list to the original target
pD2D1DeviceContext->SetTarget(pOriginalTarget);
pD2D1DeviceContext->BeginDraw();
pD2D1DeviceContext->DrawImage(pCommandList1);
pD2D1DeviceContext->EndDraw();

pD2D1DeviceContext->CreateCommandList(pCommandList2);

//draw something else to a new command list
pD2D1DeviceContext->SetTarget(pCommandList2);
pD2D1DeviceContext->BeginDraw();
pD2D1DeviceContext->RenderScene2();
pD2D1DeviceContext->EndDraw();

//draw the new command list on the old command list
pD2D1DeviceContext->SetTarget(pCommandList1);
pD2D1DeviceContext->BeginDraw();
pD2D1DeviceContext->DrawImage(pCommandList2);
pD2D1DeviceContext->EndDraw();

```

<h3><a id="Working_with_Other_APIs"></a><a id="working_with_other_apis"></a><a id="WORKING_WITH_OTHER_APIS"></a>Working with Other APIs</h3>
Direct2D employs a simple model when interoperating with GDI and Direct3D/DXGI APIs. The command list does not record these commands. It instead rasterizes the contents in place and stores them as an <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>. Because the contents are rasterized, these interop points do not maintain high fidelity.

<b>GDI:</b> The command sink interface does not support Get/ReleaseDC() calls. When a call to <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc">ID2D1GdiInteropRenderTarget::ReleaseDC</a> is made, Direct2D renders the contents of the updated  region into a <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">D2D1Bitmap</a>. This will be replayed as an aliased <a href="/windows/desktop/Direct2D/id2d1rendertarget-drawbitmap">DrawBitmap</a> call with a copy composite mode. 
To rasterize the bitmap at the correct DPI, at the time of playback of the commands, whatever DPI value is set using the SetDPI() function is used. This is the only case where the <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">sink</a> respects the SetDPI() call.


<b>DX:</b> Direct3D cannot render directly to the command list. To render Direct3D content in this case, the application can call <a href="/windows/desktop/Direct2D/id2d1rendertarget-drawbitmap">DrawBitmap</a> with the <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a> backed by a Direct3D surface.

## -see-also

<a href="/windows/desktop/direct3d11/overviews-direct3d-11-render-multi-thread-command-list">Command List</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>



<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1image">ID2D1Image</a>



<a href="/windows/desktop/Direct2D/printing-and-command-lists">Printing and Command Lists</a>
