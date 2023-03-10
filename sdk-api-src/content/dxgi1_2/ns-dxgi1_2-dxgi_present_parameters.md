---
UID: NS:dxgi1_2.DXGI_PRESENT_PARAMETERS
title: DXGI_PRESENT_PARAMETERS (dxgi1_2.h)
description: Describes information about present that helps the operating system optimize presentation.
helpviewer_keywords: ["DXGI_PRESENT_PARAMETERS","DXGI_PRESENT_PARAMETERS structure [DXGI]","direct3ddxgi.dxgi_present_parameters","dxgi1_2/DXGI_PRESENT_PARAMETERS"]
old-location: direct3ddxgi\dxgi_present_parameters.htm
tech.root: direct3ddxgi
ms.assetid: C2C69457-5415-4CAA-901B-A3A8591C6CB0
ms.date: 12/05/2018
ms.keywords: DXGI_PRESENT_PARAMETERS, DXGI_PRESENT_PARAMETERS structure [DXGI], direct3ddxgi.dxgi_present_parameters, dxgi1_2/DXGI_PRESENT_PARAMETERS
req.header: dxgi1_2.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DXGI_PRESENT_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_PRESENT_PARAMETERS
 - dxgi1_2/DXGI_PRESENT_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI1_2.h
api_name:
 - DXGI_PRESENT_PARAMETERS
---

# DXGI_PRESENT_PARAMETERS structure


## -description

Describes information about present that helps the operating system optimize presentation.

## -struct-fields

### -field DirtyRectsCount

The number of updated rectangles that you update in the back buffer for the presented frame. The operating system uses this information to optimize presentation. You can set this member to 0 to indicate that you update the whole frame.

### -field pDirtyRects

A list of updated rectangles that you update in the back buffer for the presented frame. An application must update every single pixel in each rectangle that it reports to the runtime; the application cannot assume that the pixels are saved from the previous frame. For more information about updating dirty rectangles, see Remarks. You can set this member to <b>NULL</b> if <b>DirtyRectsCount</b> is 0. An application must not update any pixel outside of the dirty rectangles.

### -field pScrollRect

 A pointer to the scrolled rectangle. The scrolled rectangle is the rectangle of the previous frame from which the runtime bit-block transfers (bitblts) content. The runtime also uses the scrolled rectangle to optimize presentation in terminal server and indirect display scenarios.

The scrolled rectangle also describes the destination rectangle, that is, the region on the current frame that is filled with scrolled content. You can set this member to <b>NULL</b> to indicate that no content is scrolled from the previous frame.

### -field pScrollOffset

A pointer to the offset of the scrolled area that goes from the source rectangle (of previous frame) to the destination rectangle (of current frame). You can set this member to <b>NULL</b> to indicate no offset.

## -remarks

This structure is used by the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">Present1</a> method.

The scroll rectangle and the list of dirty rectangles could overlap.  In this situation, the dirty rectangles take priority. Applications can then have pieces of dynamic content on top of a scrolled area. For example, an application could scroll a page and play video at the same time.

The following diagram and coordinates illustrate this example.

<img alt="Illustration of scroll and dirty rectangles overlapping" border="" src="./images/DXGIPresentParam.png"/>

``` syntax
DirtyRectsCount = 2
pDirtyRects[ 0 ] = { 10, 30, 40, 50 } // Video
pDirtyRects[ 1 ] = { 0, 70, 50, 80 } // New line
*pScrollRect = { 0, 0, 50, 70 }
*pScrollOffset = { 0, -10 }

```

Parts of the previous frame and content that the application renders are combined to produce the final frame that the operating system presents on the display screen. Most of the window is scrolled from the previous frame. The  application must update the video frame with the new chunk of content that appears due to scrolling.

The dashed rectangle shows the scroll rectangle in the current frame. The scroll rectangle is  specified by the <b>pScrollRect</b> member.
The arrow shows the scroll offset. The scroll offset is specified by the <b>pScrollOffset</b> member.
Filled rectangles show dirty rectangles that the application updated with new content. The filled rectangles are specified by the <b>DirtyRectsCount</b> and <b>pDirtyRects</b> members.

The scroll rectangle and offset are not supported for the <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_DISCARD</a> or <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_SEQUENTIAL</a> present option. Dirty rectangles and scroll rectangle are not supported for multisampled swap chains.

The actual implementation of composition and necessary bitblts is different for the bitblt model and the flip model. For more info about these models, see <a href="/windows/desktop/direct3ddxgi/dxgi-flip-model">DXGI Flip Model</a>.

For more info about the flip-model swap chain and optimizing presentation, see <a href="/windows/desktop/direct3ddxgi/dxgi-1-2-presentation-improvements">Enhancing presentation with the flip model, dirty rectangles, and scrolled areas</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-structures">DXGI Structures</a>
