---
UID: NF:d2d1effectauthor.ID2D1SourceTransform.Draw
title: ID2D1SourceTransform::Draw
author: windows-sdk-content
description: Draws the transform to the graphics processing unit (GPU)–based Direct2D pipeline.
old-location: direct2d\id2d1sourcetransform_draw.htm
tech.root: Direct2D
ms.assetid: 38EBBFB2-7A49-4386-80B3-86B44BF2FC39
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: Draw, Draw method [Direct2D], Draw method [Direct2D],ID2D1SourceTransform interface, ID2D1SourceTransform interface [Direct2D],Draw method, ID2D1SourceTransform.Draw, ID2D1SourceTransform::Draw, d2d1effectauthor/ID2D1SourceTransform::Draw, direct2d.id2d1sourcetransform_draw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1effectauthor.h
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
req.lib: D2d1.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1SourceTransform.Draw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1SourceTransform::Draw


## -description


Draws the transform to the graphics processing unit (GPU)–based Direct2D pipeline.


## -parameters




### -param target [in]

Type: <b><a href="https://msdn.microsoft.com/669a9377-248c-4a86-b447-ed117fff43a6">ID2D1Bitmap1</a>*</b>

The target to which the transform should be written.


### -param drawRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/655EBC1A-199E-40A2-A4C2-9622AFAEE0B5">D2D1_RECT_L</a>*</b>

The area within the source from which the image should be drawn.


### -param targetOrigin

Type: <b><a href="https://msdn.microsoft.com/652c0dd7-c24d-4941-ae23-2be21b53af69">D2D1_POINT_2U</a></b>

The origin within the target bitmap to which the source data should be drawn.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The implementation of the rasterizer guarantees that adding the <i>renderRect</i> to the <i>targetOrigin</i> does not exceed the bounds of the bitmap.

When implementing this method you must update the bitmap in this way: 

<ol>
<li>Call the <a href="https://msdn.microsoft.com/284c16ea-1a9f-4f13-b359-214178650add">ID2D1Bitmap::Map</a> method with the  D2D1_MAP_OPTIONS_DISCARD and D2D1_MAP_OPTIONS_WRITE
flags.</li>
<li>Update the buffer this method returns.</li>
<li>Call the <a href="https://msdn.microsoft.com/471c6e8a-4412-4efc-a7bf-688b1da7e367">ID2D1Bitmap::Unmap</a> method.</li>
</ol>
If you  set the buffer precision manually on the associated <a href="https://msdn.microsoft.com/26FB6D27-7EE0-43DA-A575-D9FF77846A16">ID2D1RenderInfo</a> object, it must handle different pixel formats in this method by calling <a href="https://msdn.microsoft.com/e94a0930-f681-47d0-8cee-bacf631ee6db">ID2D1Bitmap::GetPixelFormat</a>.  If you set the buffer precision manually, then you can rely on that format always being the one you provided.




## -see-also




<a href="https://msdn.microsoft.com/3D87A908-FC57-4AA9-A508-C402D8413363">ID2D1EffectImpl</a>



<a href="https://msdn.microsoft.com/A2B3E8E1-8F7F-4AFA-B1CE-5E8A5FCD9B70">ID2D1SourceTransform</a>
 

 

