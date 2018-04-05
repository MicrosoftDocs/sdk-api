---
UID: NF:strmif.IAMVideoCompression.get_KeyFrameRate
title: IAMVideoCompression::get_KeyFrameRate method
author: windows-driver-content
description: The get_KeyFrameRate method retrieves the current key-frame rate.
old-location: dshow\iamvideocompression_get_keyframerate.htm
old-project: DirectShow
ms.assetid: af73cfaa-3297-44a7-96a7-8805aad057e2
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IAMVideoCompression, IAMVideoCompression interface [DirectShow], get_KeyFrameRate method, IAMVideoCompression::get_KeyFrameRate, IAMVideoCompressionget_KeyFrameRate, dshow.iamvideocompression_get_keyframerate, get_KeyFrameRate method [DirectShow], get_KeyFrameRate method [DirectShow], IAMVideoCompression interface, get_KeyFrameRate,IAMVideoCompression.get_KeyFrameRate, strmif/IAMVideoCompression::get_KeyFrameRate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMVideoCompression.get_KeyFrameRate
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMVideoCompression::get_KeyFrameRate method


## -description



The <code>get_KeyFrameRate</code> method retrieves the current key-frame rate.




## -parameters




### -param pKeyFrameRate [out]

Pointer to a variable that receives the current key-frame rate. If the value is negative, the filter will use the default key-frame rate. If the value is zero, only the first frame is a key frame.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



The key-frame rate is the number of frames per key frame. For example, if the rate is 15, then a key frame occurs every 15 frames.

To determine if the filter supports this method, call the <a href="https://msdn.microsoft.com/d8ba2ba2-510a-4fb8-844e-48059ec4ef0d">IAMVideoCompression::GetInfo</a> method and check for the <b>CompressionCaps_CanKeyFrame</b> flag in the <i>pCapabilities</i> parameter. The <b>GetInfo</b> method also returns the default key-frame rate.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b7d8a98-35b8-442f-bf51-9e66fd03e2c9">IAMVideoCompression Interface</a>



<a href="https://msdn.microsoft.com/dc229333-3524-4228-ab13-a6e9619643fd">IAMVideoCompression::put_KeyFrameRate</a>
 

 

