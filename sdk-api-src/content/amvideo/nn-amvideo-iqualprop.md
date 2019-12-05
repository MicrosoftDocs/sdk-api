---
UID: NN:amvideo.IQualProp
title: IQualProp (amvideo.h)
description: The IQualProp interface provides methods for retrieving performance information from video renderers.
old-location: dshow\iqualprop.htm
tech.root: DirectShow
ms.assetid: 428dfb97-0dfa-442c-819e-291e6a58f712
ms.date: 12/05/2018
ms.keywords: IQualProp, IQualProp interface [DirectShow], IQualProp interface [DirectShow],described, IQualPropInterface, amvideo/IQualProp, dshow.iqualprop
ms.topic: interface
f1_keywords:
- amvideo/IQualProp
dev_langs:
- c++
req.header: amvideo.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IQualProp
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IQualProp interface


## -description



The <b>IQualProp</b> interface provides methods for retrieving performance information from video renderers. The values returned through the interface are reset each time the filter is stopped. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-renderer-filter">Video Renderer</a> filter and the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/full-screen-renderer-filter">Full Screen Renderer</a> filter expose this interface.

Applications can use this interface to retrieve video performance information. 




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IQualProp</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IQualProp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IQualProp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-iqualprop-get_avgframerate">get_AvgFrameRate</a>
</td>
<td align="left" width="63%">
Retrieves the average frame rate achieved.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-iqualprop-get_avgsyncoffset">get_AvgSyncOffset</a>
</td>
<td align="left" width="63%">
Retrieves the average time difference between when a frame was due for rendering and when rendering actually began (this is returned as a value in milliseconds).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-iqualprop-get_devsyncoffset">get_DevSyncOffset</a>
</td>
<td align="left" width="63%">
Retrieves the average time difference between when a frame was due for rendering and when rendering actually began (this is returned as a standard deviation).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-iqualprop-get_framesdrawn">get_FramesDrawn</a>
</td>
<td align="left" width="63%">
Retrieves the number of frames drawn since streaming started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer">get_FramesDroppedInRenderer</a>
</td>
<td align="left" width="63%">
Retrieves the number of frames dropped by the renderer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-iqualprop-get_jitter">get_Jitter</a>
</td>
<td align="left" width="63%">
Gets the jitter (variation in time) between successive frames delivered to the video renderer

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/interfaces">Interfaces</a>
 

 

