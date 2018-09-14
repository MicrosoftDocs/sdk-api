---
UID: NF:strmif.IAMVideoCompression.put_KeyFrameRate
title: IAMVideoCompression::put_KeyFrameRate
author: windows-sdk-content
description: The put_KeyFrameRate method sets the key-frame rate.
old-location: dshow\iamvideocompression_put_keyframerate.htm
tech.root: DirectShow
ms.assetid: dc229333-3524-4228-ab13-a6e9619643fd
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IAMVideoCompression interface [DirectShow],put_KeyFrameRate method, IAMVideoCompression.put_KeyFrameRate, IAMVideoCompression::put_KeyFrameRate, IAMVideoCompressionput_KeyFrameRate, dshow.iamvideocompression_put_keyframerate, put_KeyFrameRate, put_KeyFrameRate method [DirectShow], put_KeyFrameRate method [DirectShow],IAMVideoCompression interface, strmif/IAMVideoCompression::put_KeyFrameRate
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
 - IAMVideoCompression.put_KeyFrameRate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMVideoCompression::put_KeyFrameRate


## -description



The <code>put_KeyFrameRate</code> method sets the key-frame rate.




## -parameters




### -param KeyFrameRate [in]

Desired key-frame rate. If the value is negative, the filter will use the default key-frame rate. If the value is zero, only the first frame will be a key frame.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



To determine if the filter supports this method, call the <a href="https://msdn.microsoft.com/d8ba2ba2-510a-4fb8-844e-48059ec4ef0d">IAMVideoCompression::GetInfo</a> method and check for the <b>CompressionCaps_CanKeyFrame</b> flag in the <i>pCapabilities</i> parameter. The <b>GetInfo</b> method also returns the default key-frame rate.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6b7d8a98-35b8-442f-bf51-9e66fd03e2c9">IAMVideoCompression Interface</a>



<a href="https://msdn.microsoft.com/af73cfaa-3297-44a7-96a7-8805aad057e2">IAMVideoCompression::get_KeyFrameRate</a>
 

 

