---
UID: NF:segment.IMSVidVideoRenderer.get_MixerBitmap
title: IMSVidVideoRenderer::get_MixerBitmap
author: windows-sdk-content
description: The get_MixerBitmap method retrieves the static bitmap image, as an IPictureDisp type.
old-location: mstv\imsvidvideorenderer_get_mixerbitmap.htm
old-project: mstv
ms.assetid: cfcfab14-7084-4716-8955-574168cd3506
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_MixerBitmap method, IMSVidVideoRenderer.get_MixerBitmap, IMSVidVideoRenderer::get_MixerBitmap, IMSVidVideoRendererget_MixerBitmap, get_MixerBitmap, get_MixerBitmap method [Microsoft TV Technologies], get_MixerBitmap method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_mixerbitmap, segment/IMSVidVideoRenderer::get_MixerBitmap
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	segment.h
api_name:
-	IMSVidVideoRenderer.get_MixerBitmap
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidVideoRenderer::get_MixerBitmap


## -description


The <b>get_MixerBitmap</b> method retrieves the static bitmap image, as an <b>IPictureDisp</b> type.


## -parameters




### -param MixerPictureDisp






#### - ppMixerPictureDisp [out]

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



<a href="https://msdn.microsoft.com/830eff1a-e70e-440c-81be-69058d14f314">IMSVidVideoRenderer::get_MixerBitmapOpacity</a>



<a href="https://msdn.microsoft.com/a2270786-5289-4c41-898e-651ed881842b">IMSVidVideoRenderer::get_MixerBitmapPositionRect</a>



<a href="https://msdn.microsoft.com/fa9d9bea-f711-42f1-a247-322036744c44">IMSVidVideoRenderer::put_MixerBitmap</a>



<a href="https://msdn.microsoft.com/e39cf7b0-7a88-41e9-bddc-cdd0cc381996">Mixing an Image Onto the Video Window in C++</a>
 

 

