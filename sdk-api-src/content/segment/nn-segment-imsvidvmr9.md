---
UID: NN:segment.IMSVidVMR9
title: IMSVidVMR9 (segment.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005. The IMSVidVMR9 interface represents the Video Mixing Renderer Filter 9 (VMR-9) within the Video Control filter graph. The MSVidVMR9 object exposes this interface.
old-location: mstv\imsvidvmr9.htm
tech.root: mstv
ms.assetid: c96f91d4-fc6c-4422-8fc9-ea5fed10bd80
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidVMR9, IMSVidVMR9 interface [Microsoft TV Technologies], IMSVidVMR9 interface [Microsoft TV Technologies],described, IMSVidVMR9Interface, mstv.imsvidvmr9, segment/IMSVidVMR9
ms.topic: interface
f1_keywords: 
 - "segment/IMSVidVMR9"
dev_langs:
 - c++
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IMSVidVMR9
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidVMR9 interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>IMSVidVMR9</b> interface represents the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-mixing-renderer-filter-9">Video Mixing Renderer Filter 9</a> (VMR-9) within the Video Control filter graph. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695140(v=vs.85)">MSVidVMR9</a> object exposes this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidVMR9</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer</a>. <b>IMSVidVMR9</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidVMR9</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvmr9-get_allocator">get_Allocator</a>
</td>
<td align="left" width="63%">
Retrieves the application's custom allocator-presenter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvmr9-get_allocator_id">get_Allocator_ID</a>
</td>
<td align="left" width="63%">
Retrieves the identifier of the application's custom allocator-presenter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvmr9-get_suppresseffects">get_SuppressEffects</a>
</td>
<td align="left" width="63%">
Queries whether the Video Control configures the system for optimal video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvmr9-put_suppresseffects">put_SuppressEffects</a>
</td>
<td align="left" width="63%">
Specifies whether the Video Control configures the system for optimal video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidvmr9-setallocator">SetAllocator</a>
</td>
<td align="left" width="63%">
Sets a custom allocator-presenter for the VMR-9.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidVMR9)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidvideorenderer">IMSVidVideoRenderer</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

