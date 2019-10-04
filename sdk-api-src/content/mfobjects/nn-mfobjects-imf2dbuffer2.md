---
UID: NN:mfobjects.IMF2DBuffer2
title: IMF2DBuffer2 (mfobjects.h)
author: windows-sdk-content
description: Represents a buffer that contains a two-dimensional surface, such as a video frame.
old-location: mf\imf2dbuffer2.htm
tech.root: medfound
ms.assetid: BFA73B1A-F8A7-4100-9DBD-234CCA06F9F5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMF2DBuffer2, IMF2DBuffer2 interface [Media Foundation], IMF2DBuffer2 interface [Media Foundation],described, mf.imf2dbuffer2, mfobjects/IMF2DBuffer2
ms.topic: interface
f1_keywords: 
 - "mfobjects/IMF2DBuffer2"
dev_langs:
 - c++
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - mfobjects.h
api_name:
 - IMF2DBuffer2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMF2DBuffer2 interface


## -description


Represents a buffer that contains a two-dimensional surface, such as a video frame.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMF2DBuffer2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a>. <b>IMF2DBuffer2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMF2DBuffer2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer2-copy2dto">Copy2DTo</a>
</td>
<td align="left" width="63%">
Copies the buffer to another 2D buffer object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer2-lock2dsize">Lock2DSize</a>
</td>
<td align="left" width="63%">
Gives the caller access to the memory in the buffer.

</td>
</tr>
</table> 


## -remarks



This interface extends the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a> interface and adds a safer version of the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d">IMF2DBuffer::Lock2D</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer">IMF2DBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-buffers">Media Buffers</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/uncompressed-video-buffers">Uncompressed Video Buffers</a>
 

 

