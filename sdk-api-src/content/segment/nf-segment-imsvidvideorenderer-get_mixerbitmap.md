---
UID: NF:segment.IMSVidVideoRenderer.get_MixerBitmap
title: IMSVidVideoRenderer::get_MixerBitmap (segment.h)
author: windows-sdk-content
description: The get_MixerBitmap method retrieves the static bitmap image, as an IPictureDisp type.
old-location: mstv\imsvidvideorenderer_get_mixerbitmap.htm
tech.root: mstv
ms.assetid: cfcfab14-7084-4716-8955-574168cd3506
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_MixerBitmap method, IMSVidVideoRenderer.get_MixerBitmap, IMSVidVideoRenderer::get_MixerBitmap, IMSVidVideoRendererget_MixerBitmap, get_MixerBitmap, get_MixerBitmap method [Microsoft TV Technologies], get_MixerBitmap method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_mixerbitmap, segment/IMSVidVideoRenderer::get_MixerBitmap
ms.topic: method
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IMSVidVideoRenderer.get_MixerBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMSVidVideoRenderer::get_MixerBitmap


## -description


The <b>get_MixerBitmap</b> method retrieves the static bitmap image, as an <b>IPictureDisp</b> type.


## -parameters




### -param MixerPictureDisp [out]

Receives an <b>IPictureDisp</b> interface pointer. The caller must release the interface.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
No bitmap was set.

</td>
</tr>
</table>
 




## -remarks



If the static bitmap image is set, the VMR alpha-blends the bitmap onto the video image. For information about the <b>IPictureDisp</b> interface, see the Platform SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694740(v=VS.85).aspx">IMSVidVideoRenderer::get_MixerBitmapOpacity</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694741(v=VS.85).aspx">IMSVidVideoRenderer::get_MixerBitmapPositionRect</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694751(v=VS.85).aspx">IMSVidVideoRenderer::put_MixerBitmap</a>



<a href="https://msdn.microsoft.com/e39cf7b0-7a88-41e9-bddc-cdd0cc381996">Mixing an Image Onto the Video Window in C++</a>
 

 

