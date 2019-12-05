---
UID: NN:segment.IMSVidVideoRenderer2
title: IMSVidVideoRenderer2 (segment.h)
description: The IMSVidVideoRenderer2 interface represents a video renderer device.
old-location: mstv\imsvidvideorenderer2.htm
tech.root: mstv
ms.assetid: caaa2cf1-15be-47dc-82db-06915a55ba03
ms.date: 12/05/2018
ms.keywords: IMSVidVideoRenderer2, IMSVidVideoRenderer2 interface [Microsoft TV Technologies], IMSVidVideoRenderer2 interface [Microsoft TV Technologies],described, IMSVidVideoRenderer2Interface, mstv.imsvidvideorenderer2, segment/IMSVidVideoRenderer2
ms.topic: interface
f1_keywords:
- segment/IMSVidVideoRenderer2
dev_langs:
- c++
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- segment.h
api_name:
- IMSVidVideoRenderer2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidVideoRenderer2 interface


## -description



The <b>IMSVidVideoRenderer2</b> interface represents a video renderer device. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695138(v=vs.85)">MSVidVideoRenderer</a> object exposes this interface.

This interface provides access to the Video Mixing Renderer (VMR) filter. It inherits the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer</a> interface and adds support for custom allocator-presenters.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidVideoRenderer2</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer</a>. <b>IMSVidVideoRenderer2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidVideoRenderer2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer2-setallocator">_SetAllocator</a>
</td>
<td align="left" width="63%">
Specifies an allocator-presenter for the VMR.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer2-get__allocator">get__Allocator</a>
</td>
<td align="left" width="63%">
Retrieves the allocator-presenter from the VMR

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer2-get_allocator">get_Allocator</a>
</td>
<td align="left" width="63%">
Retrieves the allocator-presenter from the VMR as an <b>IUnknown</b> pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer2-get_allocator_id">get_Allocator_ID</a>
</td>
<td align="left" width="63%">
Retrieves an identifier for the VMR filter's allocator-presenter

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer2-get_suppresseffects">get_SuppressEffects</a>
</td>
<td align="left" width="63%">
Retrieves settings that control power management and visual effects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer2-put_suppresseffects">put_SuppressEffects</a>
</td>
<td align="left" width="63%">
Sets preferences for power management and visual effects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvideorenderer2-setallocator">SetAllocator</a>
</td>
<td align="left" width="63%">
Specifies an allocator-presenter for the VMR as an <b>IUnknown</b> pointer.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidVideoRenderer2)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/using-the-video-mixing-renderer">Using the Video Mixing Renderer</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

