---
UID: NF:amvideo.IFullScreenVideoEx.SetClipFactor
title: IFullScreenVideoEx::SetClipFactor (amvideo.h)
description: The SetClipFactor method specifies the clip factor, which determines how much of the video the Full Screen Renderer is allowed to clip.helpviewer_keywords: ["IFullScreenVideoEx interface [DirectShow]","SetClipFactor method","IFullScreenVideoEx.SetClipFactor","IFullScreenVideoEx::SetClipFactor","IFullScreenVideoSetClipFactor","SetClipFactor","SetClipFactor method [DirectShow]","SetClipFactor method [DirectShow]","IFullScreenVideoEx interface","amvideo/IFullScreenVideoEx::SetClipFactor","dshow.ifullscreenvideoex_setclipfactor"]
old-location: dshow\ifullscreenvideoex_setclipfactor.htm
tech.root: DirectShow
ms.assetid: 3e2cefd3-491f-4ba4-a234-047fe4e6c6cc
ms.date: 12/05/2018
ms.keywords: IFullScreenVideoEx interface [DirectShow],SetClipFactor method, IFullScreenVideoEx.SetClipFactor, IFullScreenVideoEx::SetClipFactor, IFullScreenVideoSetClipFactor, SetClipFactor, SetClipFactor method [DirectShow], SetClipFactor method [DirectShow],IFullScreenVideoEx interface, amvideo/IFullScreenVideoEx::SetClipFactor, dshow.ifullscreenvideoex_setclipfactor
f1_keywords:
- amvideo/IFullScreenVideoEx.SetClipFactor
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
- IFullScreenVideoEx.SetClipFactor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFullScreenVideoEx::SetClipFactor


## -description



The <code>SetClipFactor</code> method specifies the clip factor, which determines how much of the video the Full Screen Renderer is allowed to clip.



For example, suppose the display mode is 320 x 200 and the video is 352 x 288 pixels. Assuming the decoder cannot shrink the video, the display will clip about 25 percent of the image. The clip factor specifies the upper range that is permitted. The default value is 25%.


## -parameters




### -param ClipFactor [in]

Specifies the maximum allowable amount of the image to clip. The value is expressed as a percentage from 0 to 100.


## -returns



<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>Invalid argument.</td>
</tr>
<tr>
<td>S_OK</td>
<td>Success.</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nn-amvideo-ifullscreenvideoex">IFullScreenVideoEx Interface</a>
 

 

