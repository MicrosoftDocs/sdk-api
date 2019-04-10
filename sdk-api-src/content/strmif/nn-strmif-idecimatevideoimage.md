---
UID: NN:strmif.IDecimateVideoImage
title: IDecimateVideoImage (strmif.h)
author: windows-sdk-content
description: The IDecimateVideoImage interface specifies decimation on a decoder filter.
old-location: dshow\idecimatevideoimage.htm
tech.root: DirectShow
ms.assetid: 0d338d41-546f-41da-bc1f-b1dd74b399ef
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDecimateVideoImage, IDecimateVideoImage interface [DirectShow], IDecimateVideoImage interface [DirectShow],described, IDecimateVideoImageInterface, dshow.idecimatevideoimage, strmif/IDecimateVideoImage
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IDecimateVideoImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDecimateVideoImage interface


## -description



The <code>IDecimateVideoImage</code> interface specifies decimation on a decoder filter. The term <i>decimation</i> refers to scaling the video output down to a size smaller than the native size of the video.

Applications must not call methods on this interface. The <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a> filter uses this interface to decimate video at the video decoder.

Decoder filters that can decimate their video output should support this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDecimateVideoImage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDecimateVideoImage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDecimateVideoImage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cae80d57-d04a-4835-bb45-2198f36c0539">ResetDecimationImageSize</a>
</td>
<td align="left" width="63%">
Specifies that the decoder should no longer decimate its output image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f165e74-768f-48e3-be0f-887962ea9bfb">SetDecimationImageSize</a>
</td>
<td align="left" width="63%">
Specifies the dimensions to which the decoder should decimate its output image.

</td>
</tr>
</table> 

