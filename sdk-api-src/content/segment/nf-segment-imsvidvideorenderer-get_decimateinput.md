---
UID: NF:segment.IMSVidVideoRenderer.get_DecimateInput
title: IMSVidVideoRenderer::get_DecimateInput
author: windows-sdk-content
description: The get_DecimateInput method queries whether the Video Mixing Renderer (VMR) is currently configured to decimate the video (that is, reduce the native video size) before processing it.
old-location: mstv\imsvidvideorenderer_get_decimateinput.htm
old-project: mstv
ms.assetid: 1f533b85-175b-4381-b7a9-eac0d8e313ed
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IMSVidVideoRenderer interface [Microsoft TV Technologies],get_DecimateInput method, IMSVidVideoRenderer.get_DecimateInput, IMSVidVideoRenderer::get_DecimateInput, IMSVidVideoRendererget_DecimateInput, get_DecimateInput, get_DecimateInput method [Microsoft TV Technologies], get_DecimateInput method [Microsoft TV Technologies],IMSVidVideoRenderer interface, mstv.imsvidvideorenderer_get_decimateinput, segment/IMSVidVideoRenderer::get_DecimateInput
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
-	IMSVidVideoRenderer.get_DecimateInput
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMSVidVideoRenderer::get_DecimateInput


## -description


The <b>get_DecimateInput</b> method queries whether the Video Mixing Renderer (VMR) is currently configured to decimate the video (that is, reduce the native video size) before processing it.

This method is currently not supported.


## -parameters




### -param pDeci [out]

Receives one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The VMR is configured to decimate the video.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The VMR is not configured to decimate the video.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



This property should be set to true when the native video stream is HDTV but the system monitor is set to a lower resolution. This prevents the VMR from doing unnecessary work by processing the video at high resolution and then shrinking it.




## -see-also




<a href="https://msdn.microsoft.com/27eb53f8-ece8-43eb-8f94-b3d2d91548ad">IMSVidVideoRenderer Interface</a>



<a href="https://msdn.microsoft.com/ee410a7e-e021-408a-bf40-cb58dc8eca1c">IVMRMixerControl::GetMixingPrefs</a>



<a href="https://msdn.microsoft.com/3d0fdfac-ec7e-4e02-886b-2039c607dac7">Using the Video Mixing Renderer</a>
 

 

