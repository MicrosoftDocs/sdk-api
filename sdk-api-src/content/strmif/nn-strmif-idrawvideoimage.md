---
UID: NN:strmif.IDrawVideoImage
title: IDrawVideoImage
author: windows-sdk-content
description: Note  This interface has been deprecated.
old-location: dshow\idrawvideoimage.htm
old-project: DirectShow
ms.assetid: ff412213-60e5-43d8-8cb1-e7ae8b3ca1bc
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IDrawVideoImage, IDrawVideoImage interface [DirectShow], IDrawVideoImage interface [DirectShow],described, IDrawVideoImageInterface, dshow.idrawvideoimage, strmif/IDrawVideoImage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmif.h
api_name:
 - IDrawVideoImage
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDrawVideoImage interface


## -description



<div class="alert"><b>Note</b>  This interface has been deprecated. New applications should not use it.</div>
<div> </div>
The <code>IDrawVideoImage</code> interface enables an application to draw the same video image in multiple places simultaneously on the screen. The <a href="https://msdn.microsoft.com/7719ed9d-e3b9-4c84-b587-4e120b5cabf8">Video Renderer</a> filter exposes this interface. The Video Mixing Renderer (VMR) filter provides a better way to accomplish the same effect, through the use of multiple input streams.

To use this interface, call <b>DrawVideoImageBegin</b> to put the Video Renderer into GDI mode. Then the application can call the <b>DrawVideoImageDraw</b> method as often as necessary. The renderer simply takes the current video frame and draws it to the specified rectangle. This process is asynchronous to the delivery of frames to the renderer on the filter graph thread. The application is responsible for the frame rate at which it renders images; this rate will never be the same as the rate of the frames being delivered to the filter. In other words, calling this method is like taking a periodic shapshot of the video and putting it into a device context of your choosing at a rate of your choosing.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDrawVideoImage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDrawVideoImage</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/a39125b3-15b1-428d-aa64-c1b2bccf616a">DrawVideoImageBegin</a>
</td>
<td align="left" width="63%">
Turns off DirectDraw in preparation for a call to <a href="https://msdn.microsoft.com/cecc3ae4-f1fa-437e-b967-c54fca10b27c">DrawVideoImageDraw</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cecc3ae4-f1fa-437e-b967-c54fca10b27c">DrawVideoImageDraw</a>
</td>
<td align="left" width="63%">
Draws the specified source rectangle to the specified destination rectangle in the specified GDI device context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/051fa283-849d-494c-bebf-d7adabb807a0">DrawVideoImageEnd</a>
</td>
<td align="left" width="63%">
Turns DirectDraw back on after drawing has been performed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5b798477-9b36-4f59-b9cc-2938b5e4009f">Deprecated Interfaces</a>
 

 

