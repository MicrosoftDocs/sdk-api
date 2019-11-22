---
UID: NN:strmif.IDrawVideoImage
title: IDrawVideoImage (strmif.h)

description: Note  This interface has been deprecated.
old-location: dshow\idrawvideoimage.htm
tech.root: DirectShow
ms.assetid: ff412213-60e5-43d8-8cb1-e7ae8b3ca1bc

ms.date: 12/05/2018
ms.keywords: IDrawVideoImage, IDrawVideoImage interface [DirectShow], IDrawVideoImage interface [DirectShow],described, IDrawVideoImageInterface, dshow.idrawvideoimage, strmif/IDrawVideoImage
ms.topic: interface
f1_keywords: 
 - "strmif/IDrawVideoImage"
dev_langs:
 - c++
req.header: strmif.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IDrawVideoImage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDrawVideoImage interface


## -description



<div class="alert"><b>Note</b>  This interface has been deprecated. New applications should not use it.</div>
<div> </div>
The <code>IDrawVideoImage</code> interface enables an application to draw the same video image in multiple places simultaneously on the screen. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-renderer-filter">Video Renderer</a> filter exposes this interface. The Video Mixing Renderer (VMR) filter provides a better way to accomplish the same effect, through the use of multiple input streams.

To use this interface, call <b>DrawVideoImageBegin</b> to put the Video Renderer into GDI mode. Then the application can call the <b>DrawVideoImageDraw</b> method as often as necessary. The renderer simply takes the current video frame and draws it to the specified rectangle. This process is asynchronous to the delivery of frames to the renderer on the filter graph thread. The application is responsible for the frame rate at which it renders images; this rate will never be the same as the rate of the frames being delivered to the filter. In other words, calling this method is like taking a periodic shapshot of the video and putting it into a device context of your choosing at a rate of your choosing.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDrawVideoImage</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDrawVideoImage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDrawVideoImage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idrawvideoimage-drawvideoimagebegin">DrawVideoImageBegin</a>
</td>
<td align="left" width="63%">
Turns off DirectDraw in preparation for a call to <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idrawvideoimage-drawvideoimagedraw">DrawVideoImageDraw</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idrawvideoimage-drawvideoimagedraw">DrawVideoImageDraw</a>
</td>
<td align="left" width="63%">
Draws the specified source rectangle to the specified destination rectangle in the specified GDI device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idrawvideoimage-drawvideoimageend">DrawVideoImageEnd</a>
</td>
<td align="left" width="63%">
Turns DirectDraw back on after drawing has been performed.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/deprecated-interfaces">Deprecated Interfaces</a>
 

 

